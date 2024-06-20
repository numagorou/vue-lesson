<script setup></script>
<template>
  <h1>Vue Router</h1>
  <RouterLink :to="'/'">Home</RouterLink> |
  <RouterLink :to="{ path: '/about', query: { lang: 'ja' }, hash: '#title' }">About</RouterLink>
  <a href="https://vuejs.org">vue</a>
  <RouterView />
</template>
