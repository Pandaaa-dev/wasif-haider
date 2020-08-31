<template>
  <div class="full">
    <div class="header">
      <div id="backdrop" @click="backdropOff"></div>

      <div class="header-icon" @click="modal">
        <div class="header-icon__burger-line1"></div>
        <div class="header-icon__burger-line2"></div>
        <div class="header-icon__burger-line3"></div>
      </div>
      <div class="header-title"><div class="text">Wasif Haider</div></div>
    </div>
    <div class="modal">
      <div class="link" @click="home">
        Home<br />
        <div class="line"></div>
      </div>
      <div class="link" @click="aboutMe">
        About me<br />
        <div class="line"></div>
      </div>
      <div class="link" @click="contact">
        Contact Me<br />
        <div class="line"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    modal() {
      let modal = document.getElementsByClassName("modal");
      let backdrop = document.getElementById("backdrop");
      modal[0].className = "modal-open";
      backdrop.classList.add("backdrop");
    },
    backdropOff() {
      console.log("backdrop clicked");
      let modal = document.getElementsByClassName("modal-open");
      let backdrop = document.getElementById("backdrop");
      modal[0].className = "modal";
      backdrop.classList.remove("backdrop");
    },
    aboutMe() {
      this.backdropOff();
      this.$router.push("/about-me");
    },
    home() {
      this.backdropOff();
      this.$router.push("/");
    },
    contact() {
      this.backdropOff();
      this.$router.push("/contact-me");
    }
  }
};
</script>
<style scoped>
.line {
  margin-top: 1rem;
  width: 5rem;
  height: 2px;
  background-color: black;
}
.backdrop {
  position: fixed;
  width: 100%;
  height: 1100%;
  background-color: black;
  opacity: 0.5;
  z-index: 1;
}
.full {
  display: flex;
  flex-direction: column;
}
.modal {
  transform: translateX(-100%);
  width: 10rem;
  height: 40rem;
  position: absolute;
  top: 9.9%;
  background: white;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  transition: all 0.5s;
}
.modal-open {
  transform: translateX(0);
  width: 15rem;
  height: 40rem;
  position: absolute;
  top: 9.9%;
  background: white;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  transition: all 0.5s;
}
.link {
  margin: 1.5rem;
  font-size: 2rem;
  font-family: Rajdhani, sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.header {
  height: 4rem;
  display: flex;
  flex-direction: row;
  background-color: white;
  width: 100%;
  justify-items: flex-start;
  align-items: center;
  justify-content: left;
  transition: all;
}

.header-icon {
  display: flex;
  flex-direction: column;
  margin-right: 1rem;
  margin-left: 1rem;
  transition: all 1s;
}
.header-icon:hover {
  opacity: 0.1;
}
.header-title {
  text-align: center;
  font-family: Rajdhani, sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 1.5rem;
}

.header-icon__burger-line1,
.header-icon__burger-line2,
.header-icon__burger-line3 {
  background: #ddcfb5;
  width: 1.5rem;
  height: 0.3rem;
  border-radius: 0.25rem;
  margin: 2px;
  transition: all 0.4s;
}
</style>
