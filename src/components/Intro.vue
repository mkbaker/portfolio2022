<template>
  <div class="intro-div">
    <div class="intro-text">
      <h1>Hi, I'm <span class="my-name">Kellen</span>.</h1>
      <p>
        I'm a software engineer, musician, and artist. <br />
        I love to learn and explore every day. <br />
        Let's make something cool together. 🤘
      </p>
    </div>
    <button @click="jumpToProfile">Nice to meet you</button>
    <a target="_blank" href="https://blog.kellenbaker.com">
      Check out my tech blog ↗️
    </a>
    <div className="color-pop-low"></div>
  </div>
</template>

<script>
export default {
  name: "Intro",
  methods: {
    jumpToProfile() {
      let profile = document.getElementById("profile");
      profile.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style scoped>
.intro-div {
  min-height: 100vh;
  height: 100vh;
  margin: 1em;
}

.intro-div h1 {
  font-size: 6em;
}

.intro-div p {
  font-size: 2em;
}

.my-name {
  background: -webkit-linear-gradient(#fbc2eb, #a6c1ee);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.intro-text {
  border-left: 2px solid black;
  padding-left: 15px;
}

.color-pop-low {
  position: absolute;
  background-image: linear-gradient(
    to left,
    #fbc2eb 0%,
    #a6c1ee 51%,
    #fbc2eb 100%
  );
  height: 40%;
  width: 40%;
  right: 10%;
  transform: rotate(-45deg);
  z-index: -1;
}

@media only screen and (max-width: 700px) {
  .intro-div {
    min-height: 100vh;
    height: 100vh;
    margin: 0.5em;
  }

  .color-pop-low {
    background-image: none;
  }
}
</style>
