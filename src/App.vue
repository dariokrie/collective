<script setup lang="ts">
import headerView from './views/header-view.vue';
import agendaView from './views/agenda-view';
import updatesView from './views/updates-view'
</script>
<template>
  <header-view />
  <agenda-view />
  <updates-view />
  <router-view />
</template>