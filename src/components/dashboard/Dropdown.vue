<template>
  <div v-click-outside="close" class="relative bg-right" @click="toogleDropdown">
    <slot />

    <div
      v-show="open"
      class="absolute left-0 z-40 w-56 py-1 mt-1 origin-top-right bg-white shadow-xs"
      role="menu"
      aria-orientation="vertical"
      aria-labelledby="options-menu"
    >
      <router-link
        :to="{ name: 'home' }"
        class="block px-4 py-2 text-sm leading-5 text-black bg-gray-100 hover:text-gray-900 focus:outline-none focus:bg-gray-100 focus:text-gray-900"
        role="menuitem"
      >Home</router-link>

      <p class="mt-4 mb-2 ml-2 text-xs uppercase fc-light">Public</p>

      <router-link
        :to="{ name: 'questions.list' }"
        class="block px-4 py-1 text-sm leading-5 text-gray-200 hover:text-black focus:outline-none focus:bg-gray-100 focus:text-gray-900"
        role="menuitem"
      >
        <v-icon class="mr-1" small>mdi-earth</v-icon>Stack Overflow
      </router-link>

      <router-link
        :to="{ name: 'tags.list' }"
        class="block py-1 text-sm leading-5 text-gray-200 px-11 hover:text-black focus:outline-none focus:bg-gray-100 focus:text-gray-900"
        role="menuitem"
      >Tags</router-link>

      <router-link
        :to="{ name: 'users.list' }"
        class="block py-1 text-sm leading-5 text-gray-200 px-11 hover:text-black focus:outline-none focus:bg-gray-100 focus:text-gray-900"
        role="menuitem"
      >Users</router-link>

      <p class="mt-4 mb-2 ml-2 text-xs uppercase fc-light">Find a job</p>

      <router-link
        :to="{ name: 'home' }"
        class="block py-1 text-sm leading-5 text-gray-200 px-11 hover:text-black focus:outline-none focus:bg-gray-100 focus:text-gray-900"
        role="menuitem"
      >Jobs</router-link>

      <router-link
        :to="{ name: 'home' }"
        class="block py-1 text-sm leading-5 text-gray-200 px-11 hover:text-black focus:outline-none focus:bg-gray-100 focus:text-gray-900"
        role="menuitem"
      >Companies</router-link>

      <p class="mt-4 mb-2 ml-2 text-xs uppercase fc-light">TEAMS</p>

      <router-link
        :to="{ name: 'home' }"
        class="block text-sm leading-5 text-right text-gray-200 hover:text-black focus:outline-none focus:bg-gray-100 focus:text-gray-900"
      >What's this?</router-link>

      <router-link
        :to="{ name: 'home' }"
        class="block px-4 py-1 text-sm leading-5 text-gray-200 hover:text-black focus:outline-none focus:bg-gray-100 focus:text-gray-900"
        role="menuitem"
      >
        <v-icon small class="mr-1" color="orange darken-2">mdi-briefcase</v-icon>Free 30 Day Trial
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    open: false,
  }),
  methods: {
    toogleDropdown () {
      this.open = !this.open;
    },
    close () {
      this.open = false;
    },
  },
};
</script>

<style scoped>
.block {
  color: var(--gray);
}
</style>
