<template>
  <div class="home">
    <div class="header">
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">Michael Green</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item">
        <a class="nav-link" href="#">Projects</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Contact</a>
      </li>
      <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
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
      <p><strong class="special-text">Full Stack Devloper</strong> who builds things on the internet</p>
      </div>
    </div>
    <div id="about">
      <div class="img-holder">
        <img class="bio-img" src="..\assets\biopic.jpg" alt="">
      </div>
      <div class="bio">
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vel debitis temporibus aliquam expedita, saepe eveniet accusantium possimus eos tempora deleniti dolorem cum ex, fugit inventore laboriosam nemo magnam! Et, quae.</p>
      </div>
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
  }
};
</script>

<style scoped>
/* * {
  border: 1px solid red;
} */

p {
  margin: 0;
}

.home {
  display: flex;
  flex-wrap: wrap;
  height: 100%;
  width: 100%;
}

.header {
  height: auto;
  width: 100%;
}

.inspirational {
  font-size: 1.5rem;
  color: white;
  display: flex;
  width: 100%;
  height: fit-content;
  justify-content: center;
}

.ins-content {
  background-color: rgba(0, 0, 0, 0.5);
  text-align: center;
  padding: 0.5rem;
}

.special-text {
  font-size: 2rem;
  color: black;
  text-shadow: 0 0 8px white;
  font-family: "Lobster", cursive;
}

#about {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: black;
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
</style>

