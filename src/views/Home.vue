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
                <a class="dropdown-item" href="https://github.com/michaelgreen94" target="_blank"><i class="fab fa-github"></i>
                  Github</a>
                <a class="dropdown-item" href="https://www.linkedin.com/in/michael-green-756841b9/" target="_blank"><i
                    class="fab fa-linkedin"></i> LinkedIn</a>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="https://docs.google.com/document/d/1JFKnWHeaH96eqi0OkCwS_i0KjpMfLubLJ6NmRUUMNus/edit"
                  target="_blank"><i class="fas fa-file"></i> Resume</a>
              </div>
            </li>
          </ul>
        </div>
      </nav>
    </div>
    <div id="top"></div>
    <div class="inspirational">
      <div class="ins-content">
        <p>I'm Michael Green, a<br><strong class="special-text">Full Stack Developer</strong><br>I builds things on the
          Internet</p>
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
        <i class="devicon-html5-plain"></i>
        <i class="devicon-vuejs-plain"></i>
        <i class="devicon-nodejs-plain"></i>
        <i class="devicon-css3-plain"></i>
        <i class="devicon-javascript-plain"></i>
        <i class="devicon-csharp-line"></i>
        <i class="devicon-mysql-plain"></i>
        <i class="devicon-mongodb-plain"></i>
        <i class="devicon-dot-net-plain-wordmark"></i>
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
          <div class="bio-img">
          </div>
          </div>
        <div class="bio">
          <div class="biotext">
            <p>
              I'm a Software Developer with over 500 hours of front and back-end development from Boise Codeworks
              immersed bootcamp.
              I have A knack for problem solving, and the ability to think outside of the box. <br/> <br/> My passion for
              technology led to a career in software development after years of customer service and construction
              experience.
              I'm a highly motivated developer with strong front & back-end development skills.
            </p>
          </div>
        </div>
      </div>
    </div>
    <Projects />
    <div id="contact">
      <div class="contact-header">
        <div class="aboutbox">
          <p>CONTACT</p>
        </div>
      </div>
      <div class="contact-body">
        <div class="contact-me">
            <form method="POST" class="contact-form" :action="formSpreeTarget">
                <input v-model="email.name" type="text" placeholder="NAME" name="name"/>
                <input v-model="email.email" type="text" placeholder="YOUR EMAIL" name="_replyto">
                <input v-model="email.subject" type="text" placeholder="SUBJECT" name="subject" required />
                <textarea v-model="email.content" type="text" placeholder="CONTENT" name="content" required></textarea>
                <!-- <button type="submit" class="form-button">SEND</button> -->
                <v-layout justify-space-between="">
                <v-btn type="submit">Send</v-btn>
                <v-btn @click="clear">Clear</v-btn>
                </v-layout>
            </form>
        </div>
      </div>
        <div class="backtotop">
          <a class="nav-link btop" data-scroll="#top"><i class="fas fa-angle-double-up"></i></a>
        </div>
      <div class="contact-footer">
        <p>© 2018 Michael L. Green</p>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Projects from "@/components/Projects.vue";
export default {
  name: "home",
  data() {
    return {
      formSpreeTarget: "https://formspree.io/michael.green94@hotmail.com",
      email: {
        name: "",
        email: "",
        subject: "",
        content: ""
      }
    };
  },
  components: {
    Projects
  },
  methods: {
    clear() {
      this.email.name = "";
      this.email.email = "";
      this.email.subject = "";
      this.email.content = "";
    }
  },
  mounted() {
    document.querySelectorAll(".nav-link").forEach(a => {
      a.addEventListener("click", () =>
        document
          .querySelector(a.getAttribute("data-scroll"))
          .scrollIntoView({ behavior: "smooth" })
      );
    });
    $(window).scroll(function() {
      $(".arrow").css("opacity", 1 - $(window).scrollTop() / 250);
    });

    $(window).ready(function() {
      if ($(window).scrollTop() == 0) {
        $(".backtotop").css("display", "none");
      }
    });

    $(window).scroll(function() {
      $(".btop").css("opacity", 0 + $(window).scrollTop() / 250);
      $(".backtotop").css("display", "block");
    });
  }
};
</script>

<style scoped>
.backtotop {
  position: fixed;
  bottom: 3rem;
  right: 5rem;
  width: 4rem;
  height: 4rem;
}

.btop {
  color: black;
  background-color: rgba(255, 255, 255, 0.39);
  border-radius: 50%;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  /* border: 2px solid black; */
  font-weight: 900;
  font-size: 1.5rem;
}

.skillsbox {
  width: fit-content;
  border: 0.2rem solid black;
  padding: 0.5rem;
  color: black;
}

.aboutbox {
  width: fit-content;
  border: 0.2rem solid white;
  padding: 0.5rem;
  color: white;
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
  /* height: 10vh; */
  position: fixed;
  width: 100%;
  z-index: 1;
}

/* .navbar {
  padding: 1rem 1rem;
} */

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
  height: 100vh;
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

/* skills */

#skills {
  height: 70vh;
  width: 100%;
  background-color: white;
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
  align-items: flex-end;
  padding-bottom: 0.5rem;
}

.skill-icons {
  width: 100%;
  height: 80%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  font-size: 10rem;
}

/* about */

#about {
  height: 70vh;
  width: 100%;
  flex-wrap: wrap;
  /* display: flex;
  justify-content: center;
  align-items: center; */
  background-color: black;
}

.about-header {
  width: 100%;
  height: 20%;
  font-size: 2rem;
  font-weight: 800;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  padding-bottom: 0.5rem;
}

.about-body {
  height: 80%;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}

.contact-header {
  width: 100%;
  height: 20%;
  font-size: 2rem;
  font-weight: 800;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  padding-bottom: 0.5rem;
}

.img-holder {
  height: 100%;
  width: 40%;
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
  width: 60%;
}

.bio-img {
  height: 20rem;
  width: 20rem;
  border-radius: 50%;
  background: url("../assets/biopic2.jpg");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center center;
}

.biotext {
  width: 75%;
  height: 75%;
  /* background-color: black; */
  color: white;
  padding: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 1rem;
  font-size: 1.5rem;
}

.arrow i {
  color: white;
}

#contact {
  height: 100vh;
  width: 100%;
  flex-wrap: wrap;
  /* display: flex;
  justify-content: center;
  align-items: center; */
  background-color: black;
}

.contact-body {
  color: white;
  height: 75%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.contact-me {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 70%;
  width: 70%;
  /* background-color: #f5f5f5; */
  color: black;
}

.contact-form {
  display: flex;
  flex-flow: column;
  height: 100%;
  width: 100%;
}

.form-button {
  width: 100%;
  border: none;
  background-color: grey;
  color: white;
  text-transform: uppercase;
  cursor: pointer;
  border-radius: 0.9375rem;
  height: 2.5rem;
  /* display: flex;
  justify-content: center;
  align-items: center; */
}

input {
  width: 100%;
  margin: 1.5rem 0;
  background: rgba(0, 0, 0, 0);
  border: none;
  border-bottom: 1px solid grey;
  color: white;
}

textarea {
  width: 100%;
  margin: 1.5rem 0;
  background: rgba(0, 0, 0, 0);
  border: 1px solid grey;
  color: white;
}

::-webkit-input-placeholder {
  color: white;
  font-size: 1rem;
  letter-spacing: 2px;
}

.contact-footer {
  color: black;
  height: 5%;
  background-color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.5rem;
}

@media (max-width: 768px) {
  /* .special-text {
    font-size: 2rem;
  } */
  .skill-icons {
    font-size: 8rem;
  }
  .inspirational {
    font-size: 1.5rem;
    height: 100vh;
  }
  .img-holder {
    height: 40%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .bio-img {
    height: 13rem;
    width: 13rem;
  }
  .bio {
    height: 55%;
    width: 100%;
  }
  .biotext {
    height: 100%;
    width: 90%;
    font-size: 1.1rem;
    font-family: "Roboto", sans-serif;
  }
  #skills {
    height: 100vh;
  }
  #about {
    height: 100vh;
  }
  p {
    padding-bottom: 0;
  }
  .backtotop {
    bottom: 2rem;
    right: 2rem;
    height: 3rem;
    width: 3rem;
  }
}
</style>