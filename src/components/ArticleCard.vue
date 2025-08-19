<script setup>
import ProfileAndDate from './ProfileAndDate.vue';
import ShareButton from './ShareButton.vue';
import avatar from '../assets/images/avatar-michelle.jpg';

</script>

<template>
  <article class="article">
   <div class="article__image-wrapper">
    <img src="../assets/images/drawers.jpg" alt="Drawers" class="article__image">
   </div>
   <div class="article__content">
    <h2 class="article__title">Shift the overall look and feel by adding these wonderful touches to furniture in your home</h2>
    <p class="article__text">Ever been in a room and felt like something was missing? Perhaps it felt slightly bare and uninviting. I’ve got some simple tips to help you make any room feel complete.</p>
    <div class="article__footer">
      <ProfileAndDate 
      :image="avatar"
      name="Michelle Appleton"
      date="28 Jun 2020"
      />
      <ShareButton />
    </div>
   </div>
  </article>
</template>

<style scoped>
.article {
  display: block;
  max-width: 400px;
  background-color: var(--white);
  border-radius: 10px;
  margin-inline: var(--spacing-300);
  overflow: hidden;
}

.article__image-wrapper {
  height: 200px;
  overflow: hidden;
}

.article__image {
  object-fit: cover;
  object-position: center center;
}

.article__content {
  padding: 32px 30px 18px;
}

.article__title {
  font-size: 20px;
  letter-spacing: 0.25px;
  color: var(--gray-900);
  line-height: 1.3;
}

.article__text {
  color: var(--gray-500);
  letter-spacing: 0.02em;
  margin-top: var(--spacing-300);
}

.article__footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: var(--spacing-600);
}

@media(min-width: 768px) {
  .article {
    max-width: 730px;
    display: flex;
    margin-inline: 80px;
  }

  .article__content {
    padding-left: clamp(2rem, -0.4918rem + 6.5574vw, 2.5rem);
    padding-right: clamp(2.25rem, 1.0041rem + 3.2787vw, 2.5rem);
    padding-top: clamp(1.875rem, 5.6148rem + -8.1967vw, 2.5rem);
    padding-bottom: clamp(1.875rem, 5.6148rem + -8.1967vw, 2.5rem);
  }

  .article__footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: var(--spacing-300);
  }
}
</style>