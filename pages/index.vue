<template>
  <div class="container">
    <div class="intro">
      <div class="text">
        Hello! Would you like me to click your photo? Contact me now!
      </div>
      <div class="photo"></div>
    </div>
    <div class="question">
      <div class="one_line">So what do you want to know?</div>
      <div class="links">
        <div class="link About-me" @click="goToAbout">About me</div>
        <div class="link My-work" @click="goToMyWork">My Work</div>
        <div class="link Contact-me" @click="goToContactMe">Contact me</div>
      </div>
    </div>
    <div class="footer">
      <div class="statement">© Made by Pandaa Dev</div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    goToAbout() {
      console.log("hello");
      this.$router.push("/about-me");
    },
    goToMyWork() {
      this.$router.push("/my-work");
    },
    goToContactMe() {
      this.$router.push("/contact-me");
    }
  },
  
  
};
</script>

<style scoped>
.statement {
  color: #706e73;
  font-family: Rajdhani;
  font-weight: 700;
}
.footer {
  margin-top: 0.5rem;
  width: 100%;
  height: 3rem;
  background-color: black;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 1rem;
  padding-bottom: 1rem;
}
.question {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: Rajdhani, sans-serif;
  background-color: #cbc5b8;
  height: 5rem;
  margin-top: 1rem;
  padding-top: 2rem;
  padding-bottom: 1rem;
}
.one_line {
  font-size: 1.15rem;
  font-weight: 600;
}
.container {
  margin: 0;
  width: 100%;
}
.text {
  text-align: center;
  font-family: Rajdhani, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 2.5rem;
  margin-left: 1rem;
  margin-right: 1rem;
  color: #3a3838;
  opacity: 0.7;
  margin-top: 1.5rem;
}
.intro {
  /* margin-top: 1rem; */
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: auto;
  width: 100%;
  background: #ddcfb5;
}
.photo {
  margin: 3rem;
  height: 200px;
  width: 350px;
  background: url("../assets/wasif_hdr_28436203_1958936787753976_6109753684806074368_n.jpg");
  border-radius: 5rem;
  background-repeat: no-repeat;
  background-size: cover;
}
.links {
  display: flex;
  flex-direction: row;
  font-weight: 600;
  color: #636169;
  cursor: pointer;
}
.link {
  margin: 1rem;
}
.link:hover {
  opacity: 0.5;
}
</style>
