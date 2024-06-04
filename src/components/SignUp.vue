<script>
import axios from 'axios';
export default {
  name: 'Signup',
  data() {
    return {
      name: '',
      email: '',
      password: ''
    }
  },
  methods: {
    async signUp(event) {
      event.preventDefault();
      let result = await axios.post("http://localhost:3000/user", {
        name: this.name,
        email: this.email,
        password: this.password,
      })

      if (result.status === 200) {
        alert('Sign Up Successful!');
        localStorage.setItem("user-info", JSON.stringify(result.data));
      } else {
        console.erro('Error:', result.status, result.data);
        
      }
    }
  }
}
</script>
<template>
    <div class="flex flex-col items-center justify-center min-h-screen bg-gray-100">
      <h1 class="text-center text-2xl font-bold mb-6">Sign Up</h1>
      <form class="w-full max-w-sm bg-white p-6 rounded shadow-md" @submit="signUp">
        <div class="mb-4">
          <input
            v-model="name"
            type="text"
            placeholder="Enter Name"
            class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-blue-500"
          />
        </div>
        <div class="mb-4">
          <input
            v-model="email"
            type="email"
            placeholder="Enter Email"
            class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-blue-500"
          />
        </div>
        <div class="mb-6">
          <input
            v-model="password"
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
