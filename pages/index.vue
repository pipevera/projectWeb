<template>
  <div>
    <Navbar />
    <Header />
    <FloatWhatsapp />
    <Footer />
  </div>
</template>

<script>
import FloatWhatsapp from '~/components/FloatWhatsapp.vue';

</script>

<style>
  body {
    background-color: white;
  }
  .contenido {
    display: grid;
    min-height: 100vh;
    grid-template-rows: auto 1fr auto;
  }
</style>