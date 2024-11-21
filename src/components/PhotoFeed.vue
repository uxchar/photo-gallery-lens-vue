<script setup>
import { reactive } from "vue";
import PhotoCard from "./PhotoCard.vue";

const photos = [
  {
    localSrc: "./src/assets/images/adam-borkowski-n5MeAdr8UAo-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/a-person-walking-across-a-bridge-at-sunset-n5MeAdr8UAo",
    alt: "man walking across bridge",
    creator: "Adam Borkowski",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/bruno-aguirre-CLmYbo-btDs-unsplash.jpg",
    webSrc: "https://unsplash.com/photos/silhouette-of-buildings-CLmYbo-btDs",
    alt: "sunset in a large city",
    creator: "Bruno Aguirre",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/gabriel-miklos-CIxr7iuT8-Q-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/a-person-walking-down-a-street-CIxr7iuT8-Q",
    alt: "person walking down the street",
    creator: "Gabriel Miklós",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/marcus-dall-col-XU-mMDweXR4-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/silhouette-of-cloud-with-sunlight-XU-mMDweXR4",
    alt: "silhouette of cloud with sunlight",
    creator: "Marcus Dall Col",
    tag: "nature",
  },
  {
    localSrc: "./src/assets/images/casey-horner-UPIojcqDFfo-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/silhouette-of-city-during-sunset-UPIojcqDFfo",
    alt: "silhouette of city during sunset",
    creator: "Casey Horner",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/amogh-manjunath-HksFlo1t8iA-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/grey-cable-car-between-buildings-HksFlo1t8iA",
    alt: "grey cable car between buildings",
    creator: "Amogh Manjunath",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/elsa-guyader-q8qFaWNOHRM-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/silhouette-of-trees-during-sunset-q8qFaWNOHRM",
    alt: "silhouette of trees during sunset",
    creator: "Elsa Guyader",
    tag: "nature",
  },
  {
    localSrc: "./src/assets/images/johannes-hurtig-z-fpG7D7buk-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/aerial-photography-of-cityscape-z-fpG7D7buk",
    alt: "aerial photography of cityscape",
    creator: "Johannes Hurtig",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/adam-borkowski-SLFhsmMkW-A-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/a-yellow-train-on-the-tracks-SLFhsmMkW-A",
    alt: "a yellow train on the tracks",
    creator: "Adam Borkowski",
    tag: "city",
  },
  {
    localSrc:
      "./src/assets/images/daniele-levis-pelusi-jTknOGI18us-unsplash.jpg",
    webSrc: "https://unsplash.com/photos/photo-of-illuminated-city-jTknOGI18us",
    alt: "photo of illuminated city",
    creator: "Daniele Levis Pelusi",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/brady-cook-k1OIOwn1uJw-unsplash.jpg",
    webSrc: "https://unsplash.com/photos/sunset-over-the-horizon-k1OIOwn1uJw",
    alt: "sunset over the horizon",
    creator: "Brady Cook",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/biel-morro-d0xjEv-WJQk-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/brown-cathedral-during-daytime-d0xjEv-WJQk",
    alt: "brown cathedral during daytime",
    creator: "Biel Morro",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/rowan-heuvel-IrhXxv0g29I-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/landscape-photography-of-silhouette-of-palm-trees-during-sunset-IrhXxv0g29I",
    alt: "landscape photography of silhouette of palm trees during sunset",
    creator: "Rowan Heuvel",
    tag: "nature",
  },
  {
    localSrc: "./src/assets/images/tim-marshall-bh75y-7eYVo-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/black-rock-formation-on-sea-during-daytime-bh75y-7eYVo",
    alt: "black rock formation on sea during daytime",
    creator: "Tim Marshall",
    tag: "nature",
  },
  {
    localSrc: "./src/assets/images/zhan-zhang-Z_3ub5HQGjM-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/silhouette-of-flock-of-birds-flying-above-body-of-water-during-golden-hour-Z_3ub5HQGjM",
    alt: "silhouette of flock of birds flying above body of water during golden hour",
    creator: "Zhan Zhang",
    tag: "nature",
  },
  {
    localSrc: "./src/assets/images/martino-pietropoli-5voYtW69x0Y-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/worms-eye-view-photography-of-grey-mountain-5voYtW69x0Y",
    alt: "photography of grey mountain",
    creator: "Martino Pietropoli",
    tag: "nature",
  },
  {
    localSrc: "./src/assets/images/clay-banks-O5hfuVWgsS8-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/silhouette-of-airplane-flying-over-the-people-during-sunset-O5hfuVWgsS8",
    alt: "silhouette of airplane flying over the people during sunset",
    creator: "Clay Banks",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/lerone-pieters-Skfvy6yX1So-unsplash.jpg",
    webSrc: "https://unsplash.com/photos/bridge-Skfvy6yX1So",
    alt: "bridge in new york city",
    creator: "Lerone Pieters",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/yiran-ding-YyhXBQw4skk-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/woman-sitting-on-top-of-building-YyhXBQw4skk",
    alt: "woman sitting on top of building",
    creator: "Yiran Ding",
    tag: "city",
  },
  {
    localSrc: "./src/assets/images/lerone-pieters-vF6mSAWAzzU-unsplash.jpg",
    webSrc:
      "https://unsplash.com/photos/birds-eye-view-of-buildings-vF6mSAWAzzU",
    alt: "bird's eye view of buildings",
    creator: "Lerone Pieters",
    tag: "city",
  },
];

const photosFiltered = reactive([...photos]);

function filterPhotos(tag) {
  const filtered = photos.filter((photo) => photo.tag === tag);
  photosFiltered.length = 0;
  photosFiltered.push(...filtered);
}

function exitFilter() {
  photosFiltered.length = 0;
  photosFiltered.push(...photos);
}
</script>

<template>
  <span class="filter-section-label">Filter:</span>

  <div class="filter-container">
    <div class="first">
      <button class="filter-btn zig-zag" @click="filterPhotos('city')">
        #city
      </button>
      <button class="close-btn" @click="exitFilter()">x</button>
    </div>
    <div>
      <button class="filter-btn zig-zag" @click="filterPhotos('nature')">
        #nature
      </button>
      <button class="close-btn" @click="exitFilter()">x</button>
    </div>
  </div>
  <hr class="div-line" />
  <div class="photo-feed-container">
    <PhotoCard v-for="photo in photosFiltered" :photo="photo" />
  </div>
</template>

<style scoped>
button:hover {
  cursor: pointer;
}

.div-line {
  margin: auto 40px;
  border: 4px solid rgb(10, 10, 10);
}

.filter-container {
  display: flex;
  gap: 10px;
  margin-bottom: 40px;
  margin-top: 15px;
}

.filter-section-label {
  margin-left: 20px;
  padding: 5px 10px;
  font-variation-settings: "wght" 800;
  text-transform: uppercase;
  background-color: #fff;
}

.photo-feed-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.filter-btn {
  margin-left: 20px;
  font-size: 0.8rem;
  padding: 15px 30px;
  border: none;
  border-radius: 3px;
  background-color: rgb(10, 10, 10);
  color: #fff;
}
.close-btn {
  font-size: 1.3rem;
  border: none;
  color: red;
  background-color: transparent;
  margin-left: 2px;
  padding: 9.5px 10px;
}
.zig-zag {
  --mask: linear-gradient(#000 0 0) center/calc(100% - 8px) calc(100% - 8px)
      no-repeat,
    conic-gradient(from 135deg at top, #0000, #000 1deg 89deg, #0000 90deg) 0 0 /8px
      4px space no-repeat,
    conic-gradient(from -45deg at bottom, #0000, #000 1deg 89deg, #0000 90deg) 0
      100%/8px 4px space no-repeat,
    conic-gradient(from 45deg at left, #0000, #000 1deg 89deg, #0000 90deg) 0 0 /4px
      8px no-repeat space,
    conic-gradient(from -135deg at right, #0000, #000 1deg 89deg, #0000 90deg)
      100% 0/4px 8px no-repeat space;
  -webkit-mask: var(--mask);
  mask: var(--mask);
}
@media screen and (min-width: 768px) {
  .photo-feed-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(4, 1fr);
    margin: auto 60px;
    gap: 10px;
  }
  .filter-section-label,
  .filter-btn {
    margin-top: 10px;
    margin-left: 40px;
  }
}

@media screen and (min-width: 1100px) {
  .photo-feed-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(4, 1fr);
    margin: auto 60px;
    gap: 30px;
  }
}
</style>
