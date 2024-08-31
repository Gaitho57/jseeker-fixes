<template>
  <div v-if="isVisible" class="modal-overlay" @click.self="closeModal">
    <div class="modal-content">
      <button class="close-button" @click="closeModal">×</button>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppModal',
  props: {
    isVisible: {
      type: Boolean,
      required: true
    }
  },
  methods: {
    closeModal() {
      this.$emit('close');
    }
  }
}
</script>

<style scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.2); /* Semi-transparent dark background */
  backdrop-filter: blur(10px); /* Blurs the background */
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000; /* Ensure modal is above other content */
}

.modal-content {
  background: rgba(255, 255, 255, 0.3); /* White with transparency */
  backdrop-filter: blur(15px); /* Glass effect */
  border-radius: 15px;
  padding: 30px;
  box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37); /* Soft shadow */
  border: 1px solid rgba(255, 255, 255, 0.18); /* Border with transparency */
  max-width: 600px;
  width: 100%;
  position: relative;
}

.close-button {
  position: absolute;
  top: 15px;
  right: 15px;
  background-color: transparent;
  color: white;
  font-size: 24px;
  border: none;
  cursor: pointer;
  transition: color 0.3s ease;
}

.close-button:hover {
  color: #ff0000; /* Red color on hover */
}
</style>
