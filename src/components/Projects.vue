<template>
  <div id="projects">
    <div class="projectsheader">
      <div class="projectbox">
        <p>PROJECTS</p>
        </div>
    </div>
    <div class="carousel">
          <v-carousel hide-delimiters interval=60000 light>
              <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src"></v-carousel-item>
      </v-carousel>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data() {
    return {
      items: [
        {
          src: "../assets/bullutin.png"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg"
        }
      ]
    };
  }
};
</script>


<style>
p {
  margin: 0;
}

#projects {
  height: 70vh;
  width: 100%;
  flex-wrap: wrap;
  background-color: white;
}
.v-carousel {
  height: inherit;
  width: 85%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.projectsheader {
  height: 20%;
  width: 100%;
  font-size: 2rem;
  font-weight: 800;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  padding-bottom: 0.5rem;
}

.carousel {
  height: 80%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-size: contain;
}
.projectbox {
  width: fit-content;
  border: 0.2rem solid black;
  padding: 0.5rem;
  color: black;
}

.v-carousel__item {
  width: 70% !important;
}

:global(.v-image__image) {
  background-size: contain !important;
}

@media (max-width: 768px) {
  #projects {
    height: 100vh;
  }
  p {
    margin-bottom: 0 !important;
  }
}

@media (hover: hover) {
  .projectsheader {
    height: 100%;
    width: 40%;
    padding-top: 0;
    padding-bottom: 0;
    align-items: center;
  }
  .carousel {
    height: 100%;
    width: 50%;
  }
  #projects {
    display: flex;
  }
  .v-carousel__item {
    width: 80% !important;
  }
  p {
    margin-bottom: 0 !important;
  }
}
</style>
