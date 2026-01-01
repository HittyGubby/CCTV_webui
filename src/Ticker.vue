<script setup>

</script>

<template>
    <img src="/cctv.gif" class="logo">
    <img src="/grad.svg" class="grad-svg">
    <img src="/grad1.svg" class="grad1-svg">
    <p class="subtitle text" id="subtitle">Subticker副标题</p>
    <p class="title text" id="title">Ticker标题</p>
</template>

<style scoped>
.logo {
    position: absolute;
    height: 89px;
    border-top-left-radius: 15px;
    border-bottom-left-radius: 15px;
}

.subtitle {
    position: absolute;
    left: 168px;
    top: -32px;
    font-size: 28px;
    -webkit-text-stroke: 1px black;
    color: white;
    font-weight: bold;
    font-family: Arial, Microsoft YaHei;
    white-space: nowrap;
}

.title {
    position: absolute;
    left: 163px;
    top: -20px;
    font-size: 50px;
    letter-spacing: 1.5px;
    background-image: linear-gradient(to bottom, #004271, #022039);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
    -webkit-text-fill-color: transparent;
    -webkit-text-stroke: 0.5px white;
    filter: drop-shadow(2px 2px 2px #0006);
    font-weight: bold;
    font-family: Arial, Microsoft YaHei;
    white-space: nowrap;
}

.grad-svg {
    position: absolute;
    left: 153px;
    top: 35px;
    height: 60px;
}

.grad1-svg {
    position: absolute;
    left: 153px;
    top: 0px;
    height: 35px;
}
</style>
