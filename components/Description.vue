<template>
  <section class="max-w-[1300px] mx-auto bg-codeblack" >
    <div class="flex flex-col justify-center md:flex md:flex-row  md:items-center">
      <div class="w-full md:w-2/4 space-y-6 p-6 animate-fade-right">
        <h2 class="text-5xl text-balance text-white">Lorem ipsum dolor sit amet consectetur</h2>
        <p class="text-xl text-white">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nihil, distinctio ut ullam nisi, eos eum mollitia incidunt ratione soluta quaerat debitis eveniet quas quae doloribus earum dolorem quia id quos.</p>
        <p class="text-xl text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium amet rem accusamus nobis dolorum vitae soluta similique repudiandae odio beatae. Veniam recusandae est quo aut provident dignissimos, saepe adipisci in!</p>
       
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

