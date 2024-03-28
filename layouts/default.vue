<script lang="ts" setup></script>

<template>
  <div>
    <header>
      <div>App Logo</div>
      <nav>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/profile">Profile</NuxtLink>
        <NuxtLink to="/dashboard">Dashboard</NuxtLink>
      </nav>
    </header>
    <slot></slot>
    <footer>@Ojerinde Joel 2024</footer>
  </div>
</template>

<style scoped>
div {
  width: 40%;
}
header {
  background: #c4c2c2;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

nav {
  flex-basis: 50%;
  gap: 1rem;
  display: flex;
  justify-content: space-between;
}

footer {
  padding: 1rem 0;
  text-align: center;
  background: #999393;
}
.router-link-exact-active {
  color: blueviolet;
}
</style>
