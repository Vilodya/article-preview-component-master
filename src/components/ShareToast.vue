<script setup>
import triangle from '../assets/images/triangle.png';
import facebook from '../assets/images/icon-facebook.svg';
import twitter from '../assets/images/icon-twitter.svg';
import pinterest from '../assets/images/icon-pinterest.svg';

defineProps({
  isActive: Boolean
})
</script>

<template>
  <div class="share-toast" :class="{ 'share-toast--active': isActive }" :style="{ '--triangle-url': `url(${triangle})` }">
    <p class="share-toast__text">SHARE</p>
    <ul class="social-links">
      <li class="social-links__item">
        <a href="#" class="social-links__link" aria-label="Share on Facebook">
          <img :src="facebook" alt="Facebook">
        </a>
      </li>
      <li class="social-links__item">
        <a href="#" class="social-links__link" aria-label="Share on Twitter">
          <img :src="twitter" alt="Twitter">
        </a>
      </li>
      <li class="social-links__item">
        <a href="#" class="social-links__link" aria-label="Share on Pinterest">
          <img :src="pinterest" alt="Pinterest">
        </a>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.share-toast {
  display: flex;
  position: absolute;
  right: 0;
  bottom: 0;
  left: 0;
  padding: 28px 0 28px 30px;
  align-items: center;
  background-color: var(--gray-900);
  border-radius: 0 0 10px 10px;
  gap: var(--spacing-300);
  opacity: 0;
  transition: opacity 0.3s ease, visibility 0.3s ease;
  visibility: hidden;
  z-index: 1;
}

.share-toast--active {
  opacity: 1;
  visibility: visible;
}

.share-toast__text {
  color: var(--gray-400);
  letter-spacing: 3px;
  text-transform: uppercase;
}

.social-links {
  display: flex;
  align-items: center;
  gap: var(--spacing-200);
}

@media (width >= 768px) {
    .share-toast {
    right: -68px;
    bottom: 96px;
    left: auto;
    width: 248px;
    padding: 18px 39px;
    border-radius: 10px;
  }

  .share-toast::after {
    position: absolute;
    bottom: -12px;
    left: 112px;
    width: 24px;
    height: 12px;
    background-image: var(--triangle-url);
    content: '';
  }
}
</style>