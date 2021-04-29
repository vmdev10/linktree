<template>
  <div class="container">
    <vue-particles
      class="particles"
      color="#42b883"
      :particleOpacity="0.7"
      :particlesNumber="80"
      shapeType="circle"
      :particleSize="4"
      linesColor="#42b883"
      :linesWidth="1"
      :lineLinked="true"
      :lineOpacity="0.4"
      :linesDistance="150"
      :moveSpeed="1"
      :hoverEffect="true"
      hoverMode="grab"
      :clickEffect="true"
      clickMode="push"
    ></vue-particles>
    <div class="form-check form-switch dark-button">
      <input
        class="checkbox form-check-input"
        type="checkbox"
        @click="isChecked"
        id="input-dark-mode"
      />
      <label class="form-check-label" for="input-dark-mode"> Light mode </label>
    </div>
    <img class="profile" src="./assets/profile-1.jpg" />
    <div class="card">
      <div class="description">
        <h2 class="title">Ana Vitória</h2>
        <p class="subtitle">Front-end developer</p>
      </div>
      <div class="info-content">
        <a class="social-link btn effect" href="https://github.com/vmdev10" role="button">Github</a>
        <a class="social-link btn" href="https://www.instagram.com/mouraanav/" role="button">Instagram</a>
        <a class="social-link btn" href="https://www.linkedin.com/in/vit%C3%B3ria-moura-9924031b5/" role="button">LinkedIn</a>
        <a class="social-link btn" href="https://github.com/vmdev10/linktree/tree/master/linktree" role="button"
          >Código desta página</a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    isChecked() {
      const checkbox = document.getElementById("input-dark-mode");
      if (checkbox.checked) {
        document.querySelector("html").classList.add("light");
        document.querySelector("body").classList.add("light");
      } else {
        document.querySelector("html").classList.remove("light");
        document.querySelector("body").classList.remove("light");
      }
      return checkbox;
    },
  },
};
</script>

<style>
html,
body {
  background: #000;
  color: #fff;
}
.light {
  background: #fff;
  color: #35495e;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

@media (max-width: 1080px) {
  html {
    font-size: 93.75%;
  }
}
@media (max-width: 720px) {
  html {
    font-size: 87.5%;
  }
  .form-check {
    top: 0px;
  }
  .card {
    width: 25rem !important;
  }
}

.container {
  width: 100%;
  height: 100vh;
}

.particles {
  position: absolute;
  height: 75vh;
  width: 100%;
}

.dark-button {
  position: absolute;
  right: 1rem;
}

.card {
  width: 31.25rem;
  height: calc(100vh - 20px);

  margin: 20px auto 0;
  display: flex;
  flex-direction: column;
  align-items: center;

  font-family: "Nunito", sans-serif;

  background: radial-gradient(
    100% 100% at 0% 0%,
    rgba(255, 255, 255, 0.33) 0%,
    rgba(255, 255, 255, 0) 100%
  );
  box-shadow: 0px 4px 24px -1px rgba(0, 0, 0, 0.205);
  border-radius: 16px 50px 16px 16px;
}

.profile {
  width: 110px;
  height: 110px;
  margin: 1.2rem 0;
  border-radius: 50%;
  object-fit: cover;
  z-index: 99;

  position: absolute;
  top: 2rem;
  left: 50%;

  border: 2px solid #dedede;
  transform: translateX(-50%);
}

.description {
  position: relative;
  top: 10rem;

  display: flex;
  flex-direction: column;
  align-items: center;
}
.title {
  font-size: 2rem;
}
.subtitle {
  font-size: 1.2rem;
  font-weight: 700;
}

.info-content {
  width: 100%;
  position: relative;
  top: 25%;

  display: flex;
  flex-direction: column;
  justify-content: center;
}

.social-link {
  position: relative;
  transition: all 400ms ease;
  margin: 1rem 2.5rem;
  padding: 0.6rem 0;
  background-color: #42b883;
  color: #fff;

  font-family: "Nunito";
  font-size: 1.2rem;
  font-weight: 600 !important;

  border-radius: 16px;
}

.social-link:before {
  content: "";
  position: absolute;
  top: 0px;
  left: 0px;
  width: 0px;
  height: 3rem;
  border-radius: 16px;

  background: radial-gradient(
    100% 100% at 0% 0%,
    rgba(255, 255, 255, 0.33) 0%,
    rgba(255, 255, 255, 0) 100%
  );
  box-shadow: 0px 4px 24px -1px rgba(0, 0, 0, 0.1);
  transition: all 0.6s ease;
}
.social-link:hover {
  transform: scale(1.1);
}
.social-link:hover:before {
  width: 100%;
}
</style>
