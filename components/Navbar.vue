<template>
  <nav class="p-6 bg-purple-800">
    <div class="flex justify-between items-end max-w-[1300px] mx-auto">
      <div>
        <p class="text-5xl text-white">Fvera</p>
      </div>
      <div class="md:flex hidden space-x-6">
        <a :href="item.path" :title="item.name" class="text-2xl text-white" v-for="(item, index) in navItems" :key="index">{{ item.name }}</a>
      </div>
      <div class="md:hidden block">
        <button @click="toggleMenu">
          <img src="/images/icons/bars.svg" alt="bars" title="bars" class="w-8">
        </button>
      </div>
    </div>
    <div :class="{ 'max-h-96': isMenuOpen, 'max-h-0': !isMenuOpen }" class="overflow-hidden absolute z-50 top-[84px] left-0 w-full bg-purple-800 md:hidden transition-all duration-500 ease-in-out">
      <ul class="flex flex-col font-normal text-sm font-mont gap-2 p-4">
        <li v-for="item in navItems" :key="item.url">
          <a :href="item.path" class="block py-2 px-2 text-2xl text-white">
            {{ item.name }}
          </a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false, // Controla si el menú está abierto o cerrado
      navItems: [
        {
          name: "Inicio",
          path: "/"
        },
        {
          name: "Paginas web",
          path: "/web"
        },
        {
          name: "Proyectos",
          path: "/proyectos"
        }
      ]
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen; // Alterna la visibilidad del menú
    }
  }
}
</script>
