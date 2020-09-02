<template>
<!--<div id="app">-->
<div class="f-page padding-normal">
    <NavBar msg="" />
    <Intro msg="" />
</div>
<Section msg="" />
<Features msg="" />
<Services msg="" />

<!--</div>-->
</template>

<script>
import NavBar from './components/NavBar.vue'
import Intro from './components/Intro.vue'
import Section from './components/Section.vue'
import Features from './components/Features.vue'
import Services from './components/Services.vue'

export default {
    name: 'App',
    components: {
        NavBar,
        Intro,
        Section,
        Features,
        Services
    }
}
</script>

<style lang="scss" scoped>
@use "sass:string";

@function dpi($size) {
    @return calc(var(--modifier) * #{$size})
}

@mixin button {
    box-sizing: border-box;
    cursor: pointer;
    user-select: none;
    float: right;
    display: inline-block;
    border-radius: 4px;
    padding: dpi(0.75);
    padding-left: dpi(1);
    padding-right: dpi(1);
    box-shadow: 0px 5px 5px rgba(0, 0, 0, 0.25);
    text-transform: uppercase;
    font-weight: bold;
}

* {
    box-sizing: border-box;
    width: 100%; //1600px;
}

.padding-normal {
    padding-left: dpi(3);
    padding-right: dpi(3);
}

.padding-center {
    padding-left: 33.333%;
    padding-right: 33.333%;
    text-align: center;
}

.f-page {
    width: 100%;
    margin: 0 auto;
    background-color: rgb(15, 191, 191);
    height: dpi(30);
    display: flex;
    flex-direction: column;
    background-image: url("../public/img/BG.png");
    background-size: cover;
    box-sizing: border-box;
}

/*
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}*/
</style>
