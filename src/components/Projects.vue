<template>
  <div id="projects">
    <div class="projectsheader">
      <div class="projectbox">
        <p>PROJECTS</p>
        </div>
    </div>
    <div class="carousel">
          <v-carousel hide-delimiters interval=60000>
            <div class="projectimgs">
              <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src"></v-carousel-item>
            </div>
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


<style scoped>
p {
  margin: 0;
}
#projects {
  height: 100vh;
  width: 100%;
  flex-wrap: wrap;
  background-color: white;
}
.v-carousel {
  height: inherit;
  width: 85%;
}

.carousel {
  height: 80%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-size: contain;
}

.projectsheader {
  width: 100%;
  height: 20%;
  font-size: 2rem;
  font-weight: 800;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 1rem;
}

.projectbox {
  width: fit-content;
  border: 0.2rem solid black;
  padding: 0.5rem;
  color: black;
}

.projectimgs {
}

@media (hover: none) {
  #projects {
    height: 100vh;
  }
}
</style>
