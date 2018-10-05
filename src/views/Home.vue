<template>
  <div class="home">
    <div class="header">
      <nav class="navbar navbar-fixed-top navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand nav-link" data-scroll="#top">Michael Green</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
              <a class="nav-link" data-scroll="#skills">Skills</a>
            </li>
              <li class="nav-item">
              <a class="nav-link" data-scroll="#about">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" data-scroll="#projects">Projects</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" data-scroll="#contact">Contact</a>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" data-scroll="#app" id="navbarDropdown" role="button" data-toggle="dropdown"
                aria-haspopup="true" aria-expanded="false">
                Professional
              </a>
              <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="https://github.com/michaelgreen94" target="_blank"><i class="fab fa-github"></i> Github</a>
                <a class="dropdown-item" href="https://www.linkedin.com/in/michael-green-756841b9/" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="https://docs.google.com/document/d/1JFKnWHeaH96eqi0OkCwS_i0KjpMfLubLJ6NmRUUMNus/edit?usp=sharing" target="_blank"><i class="fas fa-file"></i> Resume</a>
              </div>
            </li>
          </ul>
        </div>
      </nav>
    </div>
    <div id="top"></div>
    <div class="inspirational">
      <div class="ins-content">
        <p>I'm Michael Green, a<br><strong class="special-text">Full Stack Developer</strong><br>I builds things on the Internet</p>
      </div>
      <div class="ska">
      <div class="skillsbelow">
        <p>C:\ npm i Skills</p>
      </div>
        <div class="arrow bounce">
          <a class="nav-link" data-scroll="#skills"><i class="fa fa-angle-down fa-1x" aria-hidden="true"></i></a>
          </div>
    </div>
      </div>
    <div id="skills">
      <div class="skills-header">
        <div class="skillsbox">
        <p>SKILLS</p>
        </div>
      </div>
      <div class="skill-icons">
      <i class="fab fa-html5"></i>
      <i class="fab fa-vuejs"></i>
      <i class="fab fa-node-js"></i>
      <i class="fab fa-css3-alt"></i>
      <i class="fab fa-js"></i>
      </div>
    </div>
    <div id="about">
      <div class="about-header">
        <div class="aboutbox">
        <p>ABOUT</p>
        </div>
      </div>
      <div class="about-body">
      <div class="img-holder">
        <img class="bio-img" src="..\assets\logo.png" alt="">
      </div>
      <div class="bio">
        <div class="biotext">
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vel debitis temporibus aliquam expedita, saepe
          eveniet accusantium possimus eos tempora deleniti dolorem cum ex, fugit inventore laboriosam nemo magnam! Et,
          quae.</p>
        </div>
      </div>
      </div>
    </div>
    <Projects/>
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
  methods: {},
  mounted() {
    document.querySelectorAll(".nav-link").forEach(a => {
      a.addEventListener("click", () =>
        document
          .querySelector(a.getAttribute("data-scroll"))
          .scrollIntoView({ behavior: "smooth" })
      );
    });
  }
};
</script>

<style scoped>
.skillsbox {
  width: fit-content;
  border: 0.2rem solid black;
  padding: 0.5rem;
  color: black;
  background-color: white;
}

.aboutbox {
  width: fit-content;
  border: 0.2rem solid black;
  padding: 0.5rem;
  color: black;
  background-color: white;
}
/* * {
  border: 1px solid red;
} */

p {
  margin: 0;
}

a:not([href]):not([tabindex]) {
  color: black;
  text-decoration: none;
  cursor: pointer;
}

/* arrow css */

.skillsbelow {
  width: 70%;
  background-color: rgba(0, 0, 0, 0.507);
  display: flex;
  padding-left: 1rem;
  /* justify-content: center; */
  text-align: left;
}

.arrow {
  width: 100%;
  display: flex;
  justify-content: center;
  align-content: center;
  color: white !important;
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

.ska a {
  color: white;
}

/* header */

.header {
  height: 10vh;
  position: fixed;
  width: 100%;
  z-index: 1;
}

.navbar {
  padding: 1rem 1rem;
}

/* hero body */

.inspirational {
  font-size: 2rem;
  background: url("../assets/background1.jpg");
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  color: white;
  display: flex;
  width: 100%;
  height: 90vh;
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

.bio-img {
  height: 20rem;
  width: 20rem;
  border-radius: 50%;
  background-color: black;
}

/* skills */

#skills {
  height: 50vh;
  width: 100%;
  background-color: grey;
  flex-wrap: wrap;
  /* display: flex;
  justify-content: center;
  align-items: center; */
  /* display: none; */
}

.skills-header {
  width: 100%;
  height: 20%;
  font-size: 2rem;
  font-weight: 800;
  display: flex;
  justify-content: center;
  align-items: center;
}

.skill-icons {
  width: 100%;
  height: 80%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
  font-size: 10rem;
}

/* about */

#about {
  height: 50vh;
  width: 100%;
  flex-wrap: wrap;
  /* display: flex;
  justify-content: center;
  align-items: center; */
  background-color: #343a40;
}

.about-header {
  width: 100%;
  height: 20%;
  font-size: 2rem;
  font-weight: 800;
  display: flex;
  justify-content: center;
  align-items: center;
}

.about-body {
  height: 80%;
  width: 100%;
  display: flex;
}

.img-holder {
  height: 100%;
  width: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.bio {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 50%;
}

.biotext {
  background-color: black;
  color: white;
  padding: 0.5rem;
  margin: 0.5rem;
}

#contact {
  background-color: #343a40;
  height: 100vh;
  width: 100%;
}

.arrow i {
  color: white;
}

@media (hover: none) {
  /* .special-text {
    font-size: 2rem;
  } */
  /* .skill-icons {
    font-size: 10rem;
  } */
  .inspirational {
    font-size: 1.5rem;
    height: 100vh;
  }
  .bio-img {
    height: 15rem;
    width: 15rem;
  }
  #skills {
    height: 100vh;
  }
  #about {
    height: 100vh;
  }
}
</style>