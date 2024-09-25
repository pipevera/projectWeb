<template>
  <section class="bg-codeblack relative" >
    <div class="max-w-[1300px] mx-auto" >
      <div class="flex flex-col justify-center md:flex md:flex-row  md:items-center">
        <div class="w-full md:w-2/4 space-y-6 p-6 animate-fade-right">
          <p class="text-lg text-white">Somos expertos en diseñar páginas web a medida, totalmente responsivas que hacen brillar tu negocio en línea, combinando creatividad y funcionalidad. </p>
          <p class="text-lg text-white">Además, mantenemos tus computadoras en perfecto estado con nuestros servicios de mantenimiento técnico, asegurando que todo funcione de forma rápida y sin interrupciones. ¡Nos apasiona llevar tu mundo digital al siguiente nivel!</p>
        </div>
        <div class="p-6 w-full md:w-2/4">
          <LottieAnimation 
            :animation-data="Animation1"
            :auto-play="true"
            :loop="true"
            :speed="1"
            ref="anim" />
          
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
  import { onMounted, ref } from "vue"
  import { LottieAnimation } from "lottie-web-vue"
  import Animation1 from "./assets/animations/Animation-1.json"

  let anim = ref()

  onMounted(() => {
    setTimeout(() => {
      console.log(anim.value.goToAndPlay(150, true))
      anim.value
    }, 500)
  })
</script>

