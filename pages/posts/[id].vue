<template>
  <Head>
    <Title> Post {{ id }} </Title>
  </Head>
  <h2>Bienvenido al Post #{{ id }}</h2>
</template>
<script setup>
//const route = useRoute();
const { id } = useRoute().params;
/*if (/^\d+$/.test(route.params.id)) {
  throw createError({
    statusCode: "500",
    statusMessage: "Param Type is Invalid",
  });
}*/
//console.log(route)
definePageMeta({
  validate: async (route) => {
    const _nuxtApp = useNuxtApp();
    if (!/^[0-9]+$/.test(route.params.id)) {
      throw createError({
        statusCode: "500",
        statusMessage: "Param Type is Invalid",
      });
    }
    return true;
    //console.log(_nuxtApp);
    //console.log(route)
    //return /^\d+$/.test(route.params.id);
  },
});
</script>
