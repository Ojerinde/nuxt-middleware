<template>
  <div class="profile-container">
    <h2 class="profile-title">My Profile</h2>
    <div class="profile-info">
      <div class="profile-avatar">
        <img
          src="https://cdn.iconscout.com/icon/free/png-512/free-avatar-370-456322.png?f=webp&w=256"
          alt="Profile Avatar"
        />
      </div>
      <div class="profile-details">
        <p><strong>Name:</strong>Joel Grace</p>
        <p><strong>Email:</strong>joel.grace@example.com</p>
        <p><strong>Location:</strong>Canada</p>
        <p><strong>Occupation:</strong>Software Developer</p>
      </div>
    </div>
    <div class="profile-bio">
      <h3>Bio</h3>
      <p>
        Hi there! I'm Joel, a passionate software developer based in Canada. I
        love coding, learning new technologies, and building cool projects.
      </p>
    </div>
  </div>
</template>

<style scoped>
.profile-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  border: 0.1rem solid blueviolet;
  border-radius: 0.3rem;
}

.profile-title {
  color: #333;
  font-size: 24px;
  margin-bottom: 10px;
}

.profile-info {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}

.profile-avatar img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-right: 20px;
}

.profile-details p {
  margin: 5px 0;
}

.profile-bio h3 {
  color: #333;
  font-size: 20px;
  margin-bottom: 10px;
}

.profile-bio p {
  line-height: 1.6;
}
</style>
