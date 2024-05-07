<template>
  <div class="container fade-in">
    <h1 :style="{ color: '#2a668d' }" class="password-match">Ubah Password</h1> <!-- Menggunakan style bindings untuk mengatur warna teks menjadi hijau -->
    <div class="password-container">
      <label :style="{ color: '#dce4e9' }" class="label" for="password">Password Baru</label>
      <input class="input-field" type="password" id="password" v-model="password">
    </div>
    <div class="password-container">
      <label :style="{ color: '#dce4e9' }" class="label" for="verifyPassword">Verifikasi Password</label>
      <input class="input-field" type="password" id="verifyPassword" v-model="verifyPassword">
    </div>
    <div v-if="password === verifyPassword">
      <p :style="{ color: '#2a668d' }" class="password-match">Passwords match!</p>
    </div>
    <div class="search-container">
      <label :style="{ color: '#dce4e9' }" class="label" for="search">Search</label>
      <input class="input-field" type="text" id="search" v-model="search">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      password: '',
      verifyPassword: '',
      search: ''
    }
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center; 
  padding: 10px;
  background-color:   #82b9e7;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.password-container {
  margin-bottom: 20px;
}

.search-container {
  margin-top: 20px;
}

.label {
  font-weight: bold;
  margin-bottom: 5px;
}

.input-field {
  width: 100%;
  padding: 10px;
  border: 1px solid #dce4e9;
  border-radius: 5px;
}

.input-field:focus {
  outline: none;
  border-color: #b4253d;
  box-shadow: 0 0 5px rgba(108, 99, 255, 0.5);
}

.password-match {
  color: green;
  font-weight: bold;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.fade-in {
  animation: fadeIn 0.5s ease-in-out;
}

</style>
