<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";

const router = useRouter();
// State
let loginForm = ref({
  name: "",
  password: "",
});

// Function to handle login form submission
const login = () => {
  // Get registered users from local storage
  const users = JSON.parse(localStorage.getItem("users"));

  // Append the new users to the
  const verifiedUser = users.find(
    (user) =>
      user.name.toLowerCase() === loginForm.value.name.toLowerCase() &&
      user.password.toLowerCase() === loginForm.value.password.toLowerCase()
  );

  // Store authentication result
  localStorage.setItem("isAuthenticated", true);
  
  if (verifiedUser) router.push("/profile");
};
</script>

<template>
  <div class="login-container">
    <h2 class="login-title">Login</h2>
    <form @submit.prevent="login">
      <div class="form-group">
        <label for="login-name">Name</label>
        <input type="text" id="login-name" v-model="loginForm.name" required />
      </div>
      <div class="form-group">
        <label for="login-password">Password</label>
        <input
          type="password"
          id="login-password"
          v-model="loginForm.password"
          required
        />
      </div>
      <button type="submit">Login</button>
    </form>
  </div>
</template>

<style scoped>
.login-container {
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

.login-title {
  color: #333;
  font-size: 24px;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input[type="text"],
input[type="password"] {
  width: 93%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  width: 100%;
  padding: 10px;
  background-color: blueviolet;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: rgb(25, 67, 111);
}
</style>
