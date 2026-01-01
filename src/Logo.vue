<script setup>

</script>

<template>
    <img src="/CCTV-1_Logo.svg" class="logo-svg">
    <p class="number text" id="number">1</p>
    <p class="name text" id="name">新&nbsp;&nbsp;闻</p>
</template>

<style scoped>
.logo-svg {
    height: 42px;
}

.number {
    position: absolute;
    left: 135px;
    top: -29px;
    font-size: 32px;
    color: #FFFFFFD0;
    letter-spacing: -2px;
    transform: scaleX(0.9);
    transform: translateX(-50%);
    font-family: Futura;
}

.name {
    position: absolute;
    left: 81px;
    top: 15px;
    font-size: 26px;
    color: #FFFFFFD0;
    font-family: 汉仪综艺体简;
    white-space: pre-wrap;
    transform: translateX(-50%);
    white-space: nowrap;
}
</style>
