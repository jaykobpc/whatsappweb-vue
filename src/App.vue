<template>
  <div id="app">
    <AppView />
    <div id="androidDialog" class="androidDialog">
      <div class="androidDialog__container">
        <h3 class="androidDialog__text">This view is only available on desktop</h3>
        <a
          @click="change_screen"
          href="https://jaykobpc.github.io/vuewhatsappmobile/index.html"
          class="androidDialog__link"
        >Switch to mobile</a>
      </div>
    </div>
  </div>
</template>

<script>
import AppView from "./components/AppView";

export default {
  name: "App",
  components: {
    AppView
  },
  mounted() {
    this.disableImageContextMenu();
    this.getDeviceWidth();
  },
  methods: {
    disableImageContextMenu() {
      var ImgTag = document.querySelectorAll("img");
      ImgTag.forEach(imgtag => {
        imgtag.addEventListener("contextmenu", e => {
          e.preventDefault();
        });
      });
    },
    change_screen() {
      window.location.href =
        "https://jaykobpc.github.io/vuewhatsappmobile/index.html";
    },
    getDeviceWidth() {
      var mobile_view = document.getElementById("androidDialog");

      window.addEventListener("resize", () => {
        if (window.innerWidth < 900) {
          mobile_view.style.display = "block";
        } else {
          mobile_view.style.display = "none";
        }
      });

      if (window.innerWidth < 900) {
        mobile_view.style.display = "block";
      } else {
        mobile_view.style.display = "none";
      }
    }
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  user-select: none;
}

html {
  scroll-behavior: smooth;
  font-size: 62.5%;
}

img {
  display: block;
  width: 100%;
}

body {
  -webkit-font-smoothing: antialiased;
  text-rendering: optimizeLegibility;
  font-family: "Segoe UI", "Helvetica Neue", Helvetica, Lucida Grande, Arial,
    Ubuntu, Cantarell, Fira Sans, sans-serif;
  -webkit-tap-highlight-color: transparent;
  overflow-x: hidden;
}

h1,
h2,
h3,
h4,
h5,
h6,
p,
span {
  font-family: inherit;
}

::-webkit-scrollbar {
  width: 6px !important;
  height: 6px !important;
}

::-webkit-scrollbar-thumb {
  background-color: rgba(0, 0, 0, 0.2);
}

::-webkit-scrollbar-track {
  background: hsla(0, 0%, 100%, 0.1);
}

.androidDialog {
  display: none;
  position: fixed;
  top: 0;
  height: 100%;
  width: 100%;
  background-image: linear-gradient(rgba(117, 158, 161, 1), rgba(48, 150, 163, 1));
  overflow: hidden;
  z-index: 100000;

  &__container {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 90%;
    background-color: #fff;
    text-align: center;
    padding: 2.5rem 1rem;
    border-radius: 0.4rem;
  }

  &__text {
    font-size: 1.5rem;
    font-weight: 600;
    color: #4a5a4a;
    margin-bottom: 2.5rem;
  }

  &__link {
    font-size: 1.5rem;
    font-weight: 400;
    background-color: #dde;
    border-radius: 0.4rem;
    color: #267c92;
    text-decoration: none;
    padding: 0.8rem 1.5rem;
    cursor: pointer;
    text-transform: uppercase;
  }
}
</style>
