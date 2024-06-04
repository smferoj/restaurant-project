<script setup>

</script>


<template>
    <div class="flex flex-col items-center justify-center min-h-screen bg-gray-100">
      <h1 class="text-center text-2xl font-bold mb-6">Sign Up</h1>
      <form class="w-full max-w-sm bg-white p-6 rounded shadow-md">
        <div class="mb-4">
          <input
            type="text"
            placeholder="Enter Name"
            class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-blue-500"
          />
        </div>
        <div class="mb-4">
          <input
            type="email"
            placeholder="Enter Email"
            class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-blue-500"
          />
        </div>
        <div class="mb-6">
          <input
            type="password"
            placeholder="Enter Password"
            class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-blue-500"
          />
        </div>
        <button
          type="submit"
          class="w-full bg-blue-500 text-white py-2 rounded hover:bg-blue-600"
        >
          Sign Up
        </button>
      </form>
    </div>
  </template>
  

  

  

<style scoped>

</style>
