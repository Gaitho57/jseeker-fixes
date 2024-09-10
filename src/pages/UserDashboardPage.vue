<template>
  <a-layout style="height: 100vh">
    <!-- Navbar -->
    <AppNavbar />

    <a-layout>
      <!-- Sidebar -->
      <a-layout-sider width="200" :style="{ background: '#555', color: 'white' }">
        <div class="sidebar">
          <ul>
            <li><a href="#" class="link">Home</a></li>
            <li><a href="#" class="link">Jobs</a></li>
            <li><a href="#" class="link">Calendar</a></li>
            <li><a href="#" class="link">Messages</a></li>
            <li><a href="#" class="link">Settings</a></li>
          </ul>
        </div>
      </a-layout-sider>

      <!-- Main Content -->
      <a-layout-content style="padding: 20px; background: #333; color: white">
        <div class="main-content">
          <div class="section">
            <h3>Job App Chart</h3>
            <!-- Chart content here -->
          </div>
          <div class="section">
            <h3>Interview Chart</h3>
            <!-- Chart content here -->
          </div>
          <div class="section">
            <h3>Skills Progress</h3>
            <!-- Skills progress content here -->
          </div>
          <div class="section">
            <h3>Upcoming Events</h3>
            <!-- Upcoming events content here -->
          </div>
        </div>
      </a-layout-content>
    </a-layout>
  </a-layout>
</template>

<script>
import AppNavbar from '@/components/AppNavbar.vue';

export default {
  name: 'UserDashboardPage',
  components: {
   AppNavbar,
  },
};
</script>

<style scoped>
.sidebar {
  background-color: #555;
  color: white;
  height: 100%;
  display: flex;
  align-items: center;
}

.sidebar ul {
  list-style-type: none;
  padding: 20px;
}

.sidebar li {
  margin-bottom: 20px;
}

.sidebar a {
  color: white;
  text-decoration: none;
}

.sidebar a:hover {
  text-decoration: underline;
}

.main-content {
  padding: 20px;
}

.section {
  border: 1px dashed white;
  margin: 10px;
  padding: 10px;
  background: #444;
}
</style>

