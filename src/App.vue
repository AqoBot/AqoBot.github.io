<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <transition
      name="custom-classes-transition"
      enter-active-class="animated fadeIn"
      leave-active-class="animated fadeOut"
    >
      <router-view class="view"/>
    </transition>
</template>

<style>
@import '@/assets/base.css';


</style>
