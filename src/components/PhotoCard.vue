<script setup>
import Image from "next/image";

const props = defineProps(["photo"]);
</script>

<template>
  <a :href="photo.webSrc" class="photo-link">
    <div class="photo-card">
      <Image :src="photo.localSrc" :alt="photo.alt" class="feed-img" />

      <p class="creator">{{ photo.creator }}</p>
    </div>
  </a>
</template>

<style scoped>
img {
  width: 80%;
  margin-top: 40px;
}

a .photo-card {
  margin: 40px auto;
}

.photo-card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #f5f5f5;
  width: 90%;
  cursor: pointer;
}

.creator {
  font-size: 0.8rem;
  margin: 15px 35px auto auto;
  padding-bottom: 30px;
  justify-content: end;
}
</style>
