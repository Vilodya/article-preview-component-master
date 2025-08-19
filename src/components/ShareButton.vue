<script setup>
import { ref } from 'vue'

const isActive = ref(false)

function toggleShare() {
  isActive.value = !isActive.value
  console.log('Share clicked! Active:', isActive.value)
}
</script>

<template>
    <button 
      class="share-button" 
      :class="{ 'share-button--active': isActive }"
      @click="toggleShare"
    >
    <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
    <circle class="share-button__circle" cx="16" cy="16" r="16" fill="currentColor"/>
    <path class="share-button__arrow" d="M24 15.495L17.7663 9.01389V12.8806H16.4409C12.3314 12.8806 9 16.0393 9 19.9358V21.9849L9.58868 21.3733C11.5901 19.2941 14.4221 18.1094 17.3912 18.1094H17.7663V21.9761L24 15.495Z" fill="currentColor"/>
    </svg>
  </button>
</template>

<style scoped>
.share-button {
  width: 32px;
  height: 32px;
  cursor: pointer;
  border-radius: 50%;
}

.share-button__circle {
  fill: var(--gray-200);
}

.share-button:hover .share-button__circle,
.share-button:focus-visible .share-button__circle {
  fill: var(--gray-500);
}

.share-button__arrow {
  fill: var(--gray-500);
}

.share-button:hover .share-button__arrow,
.share-button:focus-visible .share-button__arrow {
  fill: var(--gray-200);
}

.share-button--active .share-button__circle {
  fill: var(--gray-500);
}

.share-button--active .share-button__arrow {
  fill: var(--gray-200);
}
</style>