<script setup></script>

<template>
  <div class="nav-section">
    <div class="logo-container animate__animated animate__fadeInDown">
      <img src="/public/images/donut.png" class="logo-icon" alt="logo" />
      <h1 class="logo">lens</h1>
      <p class="logo-text">The Golden Hour Curation</p>
    </div>
    <button class="feed-btn nav-right">
      <a href="#" class="nav-right feed-link">Feed</a>
    </button>
    <button class="create-acc-btn nav-right">
      <a href="#">Create Account</a>
    </button>
  </div>
</template>

<style scoped>
.nav-section {
  position: relative;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  height: 100vh;
  margin: auto auto 150px auto;
  padding-top: 40px;
  color: #fff;
  overflow: hidden;
}

.nav-section::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
      rgba(0, 0, 0, 0),
      rgba(0, 0, 0, 0.3),
      rgba(0, 0, 0, 0.9)
    ),
    url("/public/images/adam-borkowski-SLFhsmMkW-A-unsplash.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  z-index: 0;
}

.nav-section > * {
  position: relative;
  z-index: 1;
}
a:link {
  text-decoration: none;
  font-weight: 700;
  font-size: 0.8rem;
  letter-spacing: 0.4px;
  color: #fff;
  text-align: center;
}
a:visited {
  text-decoration: none;
  color: #fff;
}
a:hover {
  text-decoration: none;
  color: #ffac07;
}
a:active {
  text-decoration: none;
}

.create-acc-btn a {
  color: #090909;
}
.create-acc-btn a:hover {
  color: #171717;
}

.logo-container {
  display: flex;
  margin-left: 25px;
}

.logo,
.logo-text {
  visibility: hidden;
}

.logo-icon {
  width: 60px;
  height: 60px;
}

.logo:hover {
  text-shadow: 1px 1px #d68e29, 2px 2px #e4a401, 4px 4px #ee9f00,
    6px 6px #fbc439, 8px 8px #ffbf5e;
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

.create-acc-btn {
  border: none;
  background-color: #ffffff;
  transition: background-color 0.5s ease;
  margin-right: 30px;
  margin-left: 20px;
  border-radius: 3px;
  height: 50px;
  padding: 10px 20px;
}
.feed-btn {
  height: 50px;
  padding: 10px 20px;
  border: none;
  background-color: rgb(9, 9, 9);
  transition: background-color 0.5s ease;
  border-radius: 3px;
  margin-left: -20%;
}

.create-acc-btn:hover {
  background-color: #ffac07;
}

@media screen and (min-width: 768px) {
  a:link {
    font-size: 0.9rem;
  }

  .nav-section {
    display: flex;
    flex-direction: row;
    margin: auto auto 150px auto;
    justify-content: space-between;
  }
  .logo-container {
    flex-direction: column;
    margin-top: -150px;
    margin-left: 40px;
  }

  .logo {
    visibility: visible;
    font-size: 6.5rem;
    font-variation-settings: "wght" 900;
    text-transform: uppercase;
    cursor: pointer;
    letter-spacing: 0.5px;
    transition: text-shadow 1s;
  }
  .logo-text {
    visibility: visible;
    font-size: 0.9rem;
    margin-left: 8px;
    margin-top: -80px;
  }
  .logo-icon {
    visibility: hidden;
  }

  .create-acc-btn {
    margin-right: 55px;

    /* padding: 25px 30px; */
  }
  .feed-btn {
    margin-left: 15%;
  }
}

@media screen and (min-width: 1100px) {
  .logo-container {
    justify-content: end;
    margin-bottom: 60px;
  }
  .logo {
    font-size: 9.5rem;
  }

  .logo-text {
    margin-top: -125px;
  }
  .feed-btn {
    margin-left: 40%;
  }
}
</style>
