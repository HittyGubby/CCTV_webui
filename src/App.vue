<script setup>
import Logo from './Logo.vue';
import Ticker from './Ticker.vue';
import { onMounted } from 'vue';
onMounted(() => {
  Array.from(document.getElementsByClassName("text")).forEach(
    (el) => {
      document.getElementById(el.id).innerHTML = localStorage.getItem(el.id) || el.innerHTML;
      el.addEventListener("click", (event) => {
        if (el.dataset.editing) return;
        el.dataset.editing = "true";
        const originalHTML = el.innerHTML;
        const editable = el.cloneNode(true);
        editable.textContent = el.innerHTML.replace(/&nbsp;/g, " ");
        editable.setAttribute("contenteditable", true);
        el.style.display = "none";
        el.parentNode.insertBefore(editable, el);
        editable.focus();
        editable.addEventListener("input", () => {
          if (editable.textContent.trim()) {
            el.innerHTML = editable.innerHTML.replace(/ /g, "&nbsp;")
            localStorage.setItem(el.id, el.innerHTML);
          }
        });
        editable.addEventListener("blur", () => {
          if (!editable.innerHTML.trim()) {
            el.innerHTML = editable.innerHTML = originalHTML;
          }
          el.style.display = "";
          delete el.dataset.editing;
          editable.remove();
        });
        event.stopPropagation();
      });
    }
  );
});
</script>

<template>
  <div class="logo-wrapper">
    <Logo />
  </div>
  <div class="ticker-wrapper">
    <Ticker />
  </div>
</template>

<style scoped>
.bg-img {
  position: absolute;
  left: 0;
  top: 0;
  height: 100%;
}

.logo-wrapper {
  position: absolute;
  left: 5.9%;
  top: 7.8%;
}

.ticker-wrapper {
  position: absolute;
  left: 5.2%;
  top: 81%;
}
</style>
