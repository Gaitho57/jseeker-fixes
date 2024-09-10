<template>
  <a-layout-header :style="{ background: '#333', padding: '0 20px', display: 'flex', justifyContent: 'space-between', alignItems: 'center', color: 'white' }">
    <div class="logo">
      <a href="#" style="color: white; font-size: 20px;">MyDashboard</a>
    </div>
    <div class="profile">
      <a-avatar icon="user" style="background-color: #fff; color: #333;" />
      <span class="username">User Name</span>
    </div>
  </a-layout-header>
</template>

<script>
export default {
  name: 'AppNavbar',
};
</script>

<style scoped>
.logo {
  font-size: 20px;
}

.profile {
  display: flex;
  align-items: center;
}

.username {
  margin-left: 10px;
}
</style>

