<script setup>
const props = defineProps({
  isActive: Boolean
})

const emit = defineEmits(['toggle'])

function handleClick() {
  emit('toggle')
}
</script>

<template>
  <button 
      class="share-button"
      :class="{ 'share-button--active': props.isActive }"
      @click="handleClick"
      aria-label="Share"
    >
    <svg xmlns="http://www.w3.org/2000/svg" width="15" height="13"><path class="share-button__icon" fill="currentColor" d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"/></svg>
  </button>
</template>

<style scoped>
  .share-button {
    display: flex;
    position: relative;
    width: 32px;
    height: 32px;
    align-items: center;
    background-color: var(--gray-200);
    border-radius: 50%;
    cursor: pointer;
    justify-content: center;
    z-index: 2;
  }

  .share-button__icon {
    fill: var(--gray-500);
  }

  .share-button:hover,
  .share-button:focus-visible,
  .share-button--active {
    background-color: var(--gray-500);
  }

  .share-button:hover .share-button__icon,
  .share-button:focus-visible .share-button__icon,
  .share-button--active .share-button__icon {
    fill: var(--gray-200);
  }
</style>