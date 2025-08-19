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
  background-color: var(--white);
  border-radius: 10px;
  margin-inline: var(--spacing-300);
  max-width: 400px;
  overflow: hidden;
}

.article__image-wrapper {
  height: 200px;
  overflow: hidden;
}

.article__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}

.article__content {
  padding: 32px 30px 18px;
}

.article__title {
  font-size: 20px;
  color: var(--gray-900);
  letter-spacing: 0.25px;
  line-height: 1.3;
}

.article__text {
  color: var(--gray-500);
  letter-spacing: 0.02em;
  margin-top: var(--spacing-300);
}

.article__footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: var(--spacing-600);
}

@media(width >= 768px) {
  .article {
    display: flex;
    margin-inline: 80px;
    max-width: 730px;
  }

  .article__image-wrapper {
    max-width: 285px;
    min-width: 230px;
    height: auto;
  }

  .article__image {
    height: 100%;
    object-fit: cover;
    object-position: left center;
  }

  .article__content {
    padding: 30px 40px;
    max-width: 445px;
  }

  .article__footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: var(--spacing-300);
  }
}
</style>