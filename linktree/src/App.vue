<template>
  <div class="container">
    <vue-particles
      class="particles"
      color="#dedede"
      :particleOpacity="0.7"
      :particlesNumber="80"
      shapeType="circle"
      :particleSize="4"
      linesColor="#dedede"
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
    <img class="profile" src="./assets/profile-1.jpg" />
    <div class="card">
      <div class="description">
        <h2 class="title">Ana Vitória</h2>
        <p class="subtitle">Desenvolvedora front-end</p>
      </div>
      <div class="info-content">
        <a class="social-link btn" href="#" role="button">E-mail</a>
        <a class="social-link btn" href="#" role="button">Github</a>
        <a class="social-link btn" href="#" role="button">LinkedIn</a>
        <a class="social-link btn" href="#" role="button">Código dessa página</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
html,
body {
  background: #35495e;
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

.card {
  width: 31.25rem;
  height: calc(100vh - 20px);

  margin: 20px auto 0;
  display: flex;
  flex-direction: column;
  align-items: center;

  font-family: "Nunito", sans-serif;

  color: #fff;

  background: radial-gradient(
    100% 100% at 0% 0%,
    rgba(255, 255, 255, 0.33) 0%,
    rgba(255, 255, 255, 0) 100%
  );
  box-shadow: 0px 4px 24px -1px rgba(0, 0, 0, 0.1);
  border-radius: 16px 50px 16px 16px;
}

.profile {
  width: 104px;
  margin-bottom: 20px;
  height: 104px;
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
  top: 9rem;

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
  margin: 1rem 2.5rem;
  padding: 0.6rem 0;
  background-color: #42b883;
  color: #fff;

  font-family: 'Nunito';
  font-weight: 600 !important;

  border-radius: 16px;
}

</style>
