<template>
  <div>
    <h1>Error Encontrado</h1>
    <h3>{{ error.statusCode }} - {{ error.statusMessage }}</h3>
    <button @click="handleError">Clean Errors</button>
  </div>
</template>

<script setup>
const route = useRoute();
const { error } = defineProps({
  error: Object,
});
console.log(route);
const path = route.path === error.path ? "/" : route.path;
const handleError = () => {
  clearError({ redirect: path });
  //console.log(error);
};
</script>

<style scoped>
div {
  text-align: center;
}
</style>
