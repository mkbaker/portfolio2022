<template>
  <div id="music" class="music-wrapper">
    <div class="music-title">
      <h1>Music</h1>
    </div>
    <div class="color-pop-wrapper">
      <div class="color-pop-right"></div>
    </div>

    <div class="projects-wrapper">
      <div class="project">
        <img src="../assets/daytrotter.png" @click="handleGranddad" />
        <div class="project-text">
          <h3>Granddad</h3>
          <p>My emo/punk/rock 'n' roll band</p>
        </div>
      </div>

      <div class="project">
        <img src="../assets/atmik.jpg" @click="handleAtmik" />
        <div class="project-text">
          <h3>Atmik</h3>
          <p>My computer music</p>
        </div>
      </div>

      <div class="project">
        <img src="../assets/sonic-pi-web-logo.png" @click="handleSonicPi" />
        <div class="project-text">
          <h3>Sonic Pi Sketches</h3>
          <p>My code</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Music",
};
</script>

<style scoped>
.music-wrapper {
  min-height: 100vh;
  max-height: 100vh;
  height: 100vh;
  /* margin: 1em; */
}
.music-title {
  position: absolute;
  right: 2vw;
  margin-top: 6em;
}
.music-title h1 {
  transform: rotate(90deg);
  font-size: 6em;
}

.color-pop-wrapper {
  position: absolute;
  right: 0;
  z-index: -1;
  padding-top: 15em;
  height: 75%;
  width: 50%;
  float: right;
}
.color-pop-right {
  float: right;
  height: 100%;
  width: 50%;
  z-index: -1;
  /* transform: rotate(90deg); */
  background-image: linear-gradient(
    to bottom,
    #fbc2eb 0%,
    #a6c1ee 51%,
    #fbc2eb 100%
  );
}

.projects-wrapper {
  padding-top: 3vh;
}
.project {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  width: 50%;
  margin: 10px;
  float: left;
}

.project-text {
  margin-top: -25px;
}

.project h3 {
  font-size: 1.5em;
  text-align: left;
  border-bottom: 2px solid black;
}

.project p {
  font-size: 1em;
  text-align: left;
}

.project img {
  min-height: 200px;
  max-height: 200px;
  min-width: 300px;
  max-width: 300px;
  height: 200px;
  width: 300px;
  padding-right: 15px;
}

img:hover {
  cursor: pointer;
}

@media only screen and (max-width: 700px) {
  .music-wrapper {
    min-height: 100vh;
    height: 100vh;
    margin: 0.5em;
    margin-top: 75%;
  }
}
</style>
