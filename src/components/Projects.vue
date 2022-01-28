<template>
  <div id="projects" class="projects-container-div">
    <div class="projects-title">
      <h1>Projects</h1>
    </div>

    <div class="project">
      <div class="project-text">
        <h3>Congressional Art Competition</h3>
        <p>Custom application built for Congresswoman Ilhan Omar.</p>
        <button @click="handleilhanSite">Click here</button>
      </div>
      <img src="../assets/ilhanSite.png" />
    </div>

    <div class="project">
      <div class="project-text">
        <h3>Blog for Dogs</h3>
        <p>
          A silly blog I made to explore routing and data management with
          Laravel.
        </p>
        <button @click="handleDogBlog">Click here</button>
      </div>
      <img
        src="https://images.unsplash.com/photo-1534361960057-19889db9621e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1500&q=80"
      />
    </div>

    <div class="project">
      <div class="project-text">
        <h3>Silent Action</h3>
        <p>
          A crowdfunding platform where users can host online auctions to
          benefit community members facing medical expenses.
        </p>
        <button @click="handleSilentAction">Click here</button>
      </div>
      <img src="../assets/silentAction.png" />
    </div>

    <div class="project">
      <div class="project-text">
        <h3>What To Say Now</h3>
        <p>
          Automated content distribution and data collection for Minneapolis
          nonprofit WithAll. This link brings you to a copy of the code I helped
          build.
        </p>
        <button @click="handleWithAll">Click here</button>
      </div>
      <img src="../assets/fiveHealthyPhrases.png" />
    </div>

    <div class="color-pop-right"></div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  methods: {
    handleDogBlog() {
      window.open("https://nameless-spire-70677.herokuapp.com/", "_blank");
    },

    handleLinkedIn() {
      window.open("https://www.linkedin.com/in/kellen-baker/", "_blank");
    },

    handleSilentAction() {
      window.open("https://silent-action.herokuapp.com/#/home", "_blank");
    },

    handleWithAll() {
      window.open("https://withall-kellen.herokuapp.com/#/home", "_blank");
    },

    handleilhanSite() {
      window.open(
        "https://congressional-art-competition.herokuapp.com/#/",
        "_blank"
      );
    },
  },
};
</script>

<style scoped>
.projects-container-div {
  min-height: 100vh;
  height: 100vh;
  /* margin: 1em; */
}

.projects-title {
  position: absolute;
  top: 230vh;
  transform: rotate(-90deg);
}

.projects-title h1 {
  font-size: 6em;
}
.project {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  width: 50%;
  margin: 10px;
  float: right;
}

.project-text {
  margin-top: -25px;
}

.project h3 {
  font-size: 1.5em;
  text-align: right;
  border-bottom: 2px solid black;
}

.project p {
  font-size: 1em;
  text-align: right;
}

.project button {
  float: right;
}

.project img {
  min-height: 200px;
  max-height: 200px;
  min-width: 300px;
  max-width: 300px;
  height: 200px;
  width: 300px;
  padding-left: 15px;
}

.color-pop-right {
  position: absolute;
  height: 50%;
  width: 60%;
  top: 300vh;
  left: 0;
  z-index: -1;
  transform: rotate(45deg);
  background-image: linear-gradient(
    to left,
    #fbc2eb 0%,
    #a6c1ee 51%,
    #fbc2eb 100%
  );
}

@media only screen and (max-width: 700px) {
  .projects-container-div {
    min-height: 100vh;
    height: 100vh;
    margin: 0.5em;
    margin-top: 75%;
  }
  .projects-title {
    position: absolute;
    top: 225vh;
    transform: none;
  }

  .project {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    margin: 10px;
  }

  .project img {
    order: 1;
    width: 100%;
    height: auto;
  }

  .project .project-text {
    order: 2;
  }
}
</style>
