<template>
  <div class="home">
    <div class="header">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="#">Michael Green</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
              <a class="nav-link" href="#">Skills</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Projects</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Contact</a>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown"
                aria-haspopup="true" aria-expanded="false">
                Professional
              </a>
              <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="#"><i class="fab fa-github"></i> Github</a>
                <a class="dropdown-item" href="#"><i class="fab fa-linkedin"></i> LinkedIn</a>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="#"><i class="fas fa-file"></i> Resume</a>
              </div>
            </li>
          </ul>
        </div>
      </nav>
    </div>
    <div class="inspirational">
      <div class="ins-content">
        <p>I'm Michael Green, a<br><strong class="special-text">Full Stack Developer</strong><br>I builds things on the Internet</p>
      </div>
      <div class="ska">
      <div class="skillsbelow">
        <p>C:\ npm i Skills</p>
      </div>
        <div class="arrow bounce"><i class="fa fa-angle-down fa-2x" aria-hidden="true"></i></div>
    </div>
      </div>
    <div class="empty-space">
      <p>nothing here</p>
    </div>
    <div id="about">
      <div class="img-holder">
        <!-- <img class="bio-img" src="..\assets\biopic.jpg" alt=""> -->
      </div>
      <div class="bio">
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vel debitis temporibus aliquam expedita, saepe
          eveniet accusantium possimus eos tempora deleniti dolorem cum ex, fugit inventore laboriosam nemo magnam! Et,
          quae.</p>
      </div>
    </div>
    <div class="carasouelbackground">
      <v-carousel id="projects">
        <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src"></v-carousel-item>
      </v-carousel>
    </div>
    <div id="contact">
      <p>contact info</p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Projects from "@/components/Projects.vue";

export default {
  name: "home",
  components: {
    Projects
  },
  data() {
    return {
      items: [
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg"
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
  },
  methods: {}
};
</script>

<style scoped>
/* * {
  border: 1px solid red;
} */

p {
  margin: 0;
}

.skillsbelow {
  width: 100%;
  display: flex;
  justify-content: center;
  align-content: center;
}

@-moz-keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    -moz-transform: translateY(0);
    transform: translateY(0);
  }
  40% {
    -moz-transform: translateY(-30px);
    transform: translateY(-30px);
  }
  60% {
    -moz-transform: translateY(-15px);
    transform: translateY(-15px);
  }
}
@-webkit-keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  40% {
    -webkit-transform: translateY(-30px);
    transform: translateY(-30px);
  }
  60% {
    -webkit-transform: translateY(-15px);
    transform: translateY(-15px);
  }
}
@keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    -moz-transform: translateY(0);
    -ms-transform: translateY(0);
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  40% {
    -moz-transform: translateY(-30px);
    -ms-transform: translateY(-30px);
    -webkit-transform: translateY(-30px);
    transform: translateY(-30px);
  }
  60% {
    -moz-transform: translateY(-15px);
    -ms-transform: translateY(-15px);
    -webkit-transform: translateY(-15px);
    transform: translateY(-15px);
  }
}

.bounce {
  -moz-animation: bounce 2s infinite;
  -webkit-animation: bounce 2s infinite;
  animation: bounce 2s infinite;
}

.ska {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  width: 100%;
  height: 30%;
}

/* .home {
  display: flex;
  flex-wrap: wrap;
  height: 100%;
  width: 100%;
} */

.header {
  height: auto;
  width: 100%;
}

.inspirational {
  font-size: 2rem;
  background: url("../assets/background1.jpg");
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  color: white;
  display: flex;
  width: 100%;
  height: 75vh;
  /* justify-content: center;
  align-items: center; */
  flex-wrap: wrap;
}

.ins-content {
  /* background-color: rgba(0, 0, 0, 0.5); */
  display: flex;
  text-align: center;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 70%;
  /* padding: 0.5rem; */
}

.special-text {
  font-size: 3rem;
  color: black;
  text-shadow: 0 0 8px white;
  font-family: "Lobster", cursive;
}

@media (hover: none) {
  /* .special-text {
    font-size: 2rem;
  } */
  .inspirational {
    font-size: 1.5rem;
    height: 95vh;
  }
}

.empty-space {
  height: 66vh;
  width: 100%;
  color: transparent;
  /* display: none; */
}

.v-carousel {
  height: 45vh;
  width: 75%;
}

#about {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #343a40;
}

.img-holder {
  width: 50%;
}

.bio-img {
  height: 50%;
  width: 50%;
}

.bio {
  width: 50%;
}

#contact {
  background-color: #343a40;
  height: 66vh;
  width: 100%;
}
</style>