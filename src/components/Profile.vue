<template>
  <div id="profile" class="profile-div">
    <div class="color-pop-left"></div>
    <div class="headshot-div">
      <img src="../assets/headshot.jpg" alt="head shot" />
    </div>
    <div class="profile-text-outer-div">
      <h1>Me</h1>
      <div class="profile-text-inner-div">
        <p>
          I'm a full stack software developer and a lifelong musician. I live in
          the Twin Cities, but I'm originally from Nome, Alaska. I like working
          with Vue, Node, and MongoDB or PostgreSQL. I enjoy developing
          beautiful, thoughtful applications, and I love writing the logic that
          makes them work. More broadly, I'm interested in the intersection of
          art, music, and technology. I'm an avid reader and listener, and I try
          to visit a new place every year. I love techno and punk music, and I'm
          a dog person.
        </p>

        <div class="actions">
          <div class="buttons">
            <!-- <a
              target="_blank"
              href="https://kellenbakerdotcom.s3.amazonaws.com/resume+11.11.21.pdf"
            >
              <button>Resume</button>
            </a> -->
            <button @click="jumpToProjects">Projects</button>
            <button @click="jumpToMusic">Music</button>
            <!-- <button>Contact me</button> -->
          </div>
          <div class="icons">
            <a href="https://gitlab.com/mkellenbaker" target="_blank">
              <vue-feather type="gitlab"></vue-feather>
            </a>

            <a href="https://github.com/mkbaker" target="_blank">
              <vue-feather type="github"></vue-feather>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Profile",
  methods: {
    jumpToProjects() {
      let projects = document.getElementById("projects");
      projects.scrollIntoView({ behavior: "smooth" });
    },
    jumpToMusic() {
      let music = document.getElementById("music");
      music.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style scoped>
.profile-div {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  min-height: 100vh;
  height: 100vh;
}
.color-pop-left {
  position: absolute;
  height: 150vh;
  width: 20vw;
  left: 0;
  top: 100vh;
  background-image: linear-gradient(#fbc2eb 0%, #a6c1ee 51%, #fbc2eb 100%);
  z-index: -1;
}

.headshot-div img {
  width: auto;
  height: 400px;
}

.profile-text-outer-div {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  /* font-size: 0.5em; */
  width: 50%;
}

.profile-text-outer-div h1 {
  transform: rotate(-90deg);
  font-size: 3em;
  align-self: flex-end;
  margin-bottom: 50%;
  background: -webkit-linear-gradient(#fbc2eb, #a6c1ee);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.profile-text-inner-div p {
  border-left: 2px solid black;
  padding-left: 10px;
}

.profile-text-inner-div button {
  flex: 1 1 auto;
  margin: 10px;
  padding: 10px;
  text-align: center;
  /* font-size: 2em; */
  transition: 0.5s;
  background-size: 200% auto;
  color: white;
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
  background-image: linear-gradient(
    to right,
    #fbc2eb 0%,
    #a6c1ee 51%,
    #fbc2eb 100%
  );
}

.actions {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.icons {
  width: 30%;
  display: flex;
  flex-direction: row;
  justify-content: end;
}

.icons i {
  margin: 10px;
}

@media only screen and (max-width: 700px) {
  .profile-div {
    min-height: 100vh;
    height: 100vh;
    display: flex;
    flex-direction: column;
  }

  .headshot-div {
    margin: 0;
  }

  .profile-text-outer-div {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    width: 100%;
  }

  .profile-text-outer-div h1 {
    background: black;
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }
}
</style>
