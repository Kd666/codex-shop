<script setup>
import { ref } from 'vue'
const isMenuOpen = ref(false)
const closeMenu = () => { isMenuOpen.value = false }
</script>
<template><header class="site-header"><a class="brand" href="#top" aria-label="月见里首页"><span>月见里</span><small>TSUKIMI</small></a><button class="menu-toggle" :aria-label="isMenuOpen ? '关闭导航' : '打开导航'" :aria-expanded="isMenuOpen" @click="isMenuOpen = !isMenuOpen"><i></i><i></i></button><nav class="nav" :class="{ open: isMenuOpen }" aria-label="主导航"><a href="#story" @click="closeMenu">关于我们</a><a href="#menu" @click="closeMenu">当季菜单</a><a href="#space" @click="closeMenu">餐厅空间</a><a class="nav-book" href="#booking" @click="closeMenu">预订座位 <b>↗</b></a></nav></header></template>
