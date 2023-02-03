<template>
  <div>
    <h1>Product details {{ id }}</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae, quia!</p>
  </div>
</template>

<script setup>
const { id } = useRoute().params
</script>

<style scoped></style>
