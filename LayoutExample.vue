<template>
  <div class="flex flex-col h-screen">
    <header class="bg-gray-900 py-6">
      <nav class="container mx-auto flex items-center justify-between px-6">
        <div class="flex items-center">
          <h1 class="text-white text-xl font-medium">My App</h1>
        </div>
        <div class="block lg:hidden">
          <button @click="isOpen = !isOpen" class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white">
            <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <title>Menu</title>
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/>
            </svg>
          </button>
        </div>
        <div :class="['hidden lg:block', { 'block': isOpen }]">
          <ul class="flex justify-end">
            <li class="mx-3">
              <a class="inline-block text-teal-200 hover:text-white" href="#">Home</a>
            </li>
            <li class="mx-3">
              <a class="inline-block text-teal-200 hover:text-white" href="#">About</a>
            </li>
            <li class="mx-3">
              <a class="inline-block text-teal-200 hover:text-white" href="#">Contact</a>
            </li>
          </ul>
        </div>
      </nav>
    </header>
    <aside class="bg-gray-800 w-64 p-6 hidden lg:block">
      <ul>
        <li class="mb-4">
          <a class="text-teal-200 hover:text-white block" href="#">Home</a>
        </li>
        <li class="mb-4">
          <a class="text-teal-200 hover:text-white block" href="#">About</a>
        </li>
        <li class="mb-4">
          <a class="text-teal-200 hover:text-white block" href="#">Contact</a>
        </li>
      </ul>
    </aside>
    <main class="container mx-auto px-6 py-10">
      <h1 class="text-3xl font-medium mb-6">Welcome to My App</h1>
      <p class="text-gray-500">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam viverra euismod odio, gravida pellentesque urna varius vitae.
      </p>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    }
  }
}
</script>

<style>

</style>
