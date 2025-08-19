<script setup>

defineProps({
  image: String,
  name: String,
  date: String,
})
</script>

<template>
  <div class="profile">
    <div class="profile__avatar">
      <img :src="image" :alt="name" />
    </div>
    <div class="profile__info">
      <div class="profile__author">{{ name }}

</div>
      <div class="profile__date">{{ date }}

</div>
    </div>
  </div>
</template>

<style scoped>
.profile {
  display: flex;
  align-items: center;
  gap: var(--spacing-200);
}

.profile__avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  overflow: hidden;
}

.profile__avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.profile__author {
  color: var(--gray-900);
  font-weight: var(--font-weight-700);
  letter-spacing: 0.02em;
}

.profile__date {
  color: var(--gray-400);
  font-weight: var(--font-weight-600);
  letter-spacing: 0.02em;
}
</style>