<template>
  <section class="relative h-[calc(100vh-88px)]">
    <!-- Imagen de fondo -->
    <div class="fixed z-0 inset-0 bg-[url('/images/home/banner.jpg')] bg-cover bg-center"></div>
    
    <!-- Capa negra semitransparente -->
    <div class="absolute inset-0 bg-black bg-opacity-50"></div>
    
    <!-- Contenido del banner -->
    <div class="relative flex flex-col w-full h-full justify-center items-center max-w-[1300px] mx-auto text-center space-y-4 md:px-40 text-white p-6 animate-fade-up animate-duration-[2000ms]">
      <h1 class=" text-3xl md:text-5xl">LOGO</h1>
      <h2 class="text-lg">Desde el diseño de sitios web modernos hasta el mantenimiento de tus equipos, te brindamos el soporte tecnológico que tu negocio necesita para crecer.</h2>
      <div class="space-x-4" >
        <button class="rounded-md bg-codeblack px-6 py-3 hover:bg-blue-900 transition" >
          Servicios
        </button>
      </div>
    </div>
  </section>
</template>


<script>
  export default {
    
  }
</script>