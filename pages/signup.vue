<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";

const router = useRouter();

// State
let signupForm = ref({
  name: "",
  password: "",
});

// Function to handle signup form submission
const signup = () => {
  // Get registered users from local storage
  const users = JSON.parse(localStorage.getItem("users")) || [];

  // Append the new users to the
  const updatedUsers = users.concat(signupForm.value);

  // Store existing and new users back to local storage
  localStorage.setItem("users", JSON.stringify(updatedUsers));

  // Redirect
  router.push("/login");
};
</script>

<template>
  <div class="signup-container">
    <h2 class="signup-title">Signup</h2>
    <form @submit.prevent="signup">
      <div class="form-group">
        <label for="signup-name">Name</label>
        <input
          type="text"
          id="signup-name"
          v-model="signupForm.name"
          required
        />
      </div>
      <div class="form-group">
        <label for="signup-password">Password</label>
        <input
          type="password"
          id="signup-password"
          v-model="signupForm.password"
          required
        />
      </div>
      <button type="submit">Signup</button>
    </form>
  </div>
</template>

<style scoped>
.signup-container {
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

.signup-title {
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
