<template>
  <div>
    <Navbar />
    <main class="container p-3 my-5 border rounded shadow">
      <slot />
    </main>
    <Footer />
  </div>
</template>

<script setup>
//<link   integrity="sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM" crossorigin="">
useHead({
  titleTemplate: "%s - Intro Nuxt",
  bodyAttrs: [
    {
      class: "text-center",
    },
  ],
  link: [
    {
      rel: "stylesheet",
      href: "https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css",
      integrity:
        "sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM",
      crossorigin: "anonymous",
    },
  ],
  script: [
    {
      src: "https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js",
      //body: "true", por si se necesita ejecutar después del body
    },
  ],
});
</script>
