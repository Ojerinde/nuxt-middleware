<script setup>
// Anonymous middleware
// definePageMeta({
//   middleware: defineNuxtRouteMiddleware((to, from) => {
//     console.log("anonymous middleware");
//     console.log("to", to);
//     console.log("from", from);
//   }),
// });
</script>

<template>
  <div class="home">
    <h2>Welcome to the homepage</h2>
    <div>
      <NuxtLink to="/login">Login</NuxtLink>
      <NuxtLink to="/signup">Signup</NuxtLink>
    </div>
  </div>
</template>

<style scoped>
.home {
  border: 0.1rem solid blueviolet;
  border-radius: 0.3rem;
  padding: 1rem 2rem;
  text-align: center;
}
h2 {
  color: blueviolet;
  font-size: 1.5rem;
}

.home div {
  display: flex;
  justify-content: space-around;
}

a {
  border-radius: 1rem;
  padding: 2rem;
  letter-spacing: 0.1rem;
  font-weight: bold;
  font-size: 1.3rem;
  background: blueviolet;
  cursor: pointer;
  text-decoration: none;
  color: white;
}
</style>
