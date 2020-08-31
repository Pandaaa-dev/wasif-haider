<template>
  <div class="about-me">
    <div class="row first">
      <div class="text">
        I am a photographer based in Bangladesh who loves to take pictures of
        wildfire and of different emotional aspects. I think pictures connect
        people.
      </div>
      <div class="pic firstpic">
        <img class="firstimg" src="~assets/spoons.jpg" alt="" />
      </div>
    </div>
    <div class="row second">
      <div class="pic secondpic">
        <img class="secondimg" src="~assets/baloon.jpg" alt="" />
      </div>
      <div class="text">
        They connect people by giving them a sense of togetherness.And hopefully
        one day my pictures will too!
      </div>
    </div>
    <div class="last-line">
      Wanna see <span class="more" @click="$router.push('/my-work')"> more </span> of my pictures?
    </div>
    <div class="footer">
      <div class="statement">© Made by Pandaa Dev</div>
    </div>
  </div>
</template>
<script>
export default {};
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
.more {
  font-weight: 600;

}
.more:hover{
  opacity: 0.5;
}
.last-line {
  text-align: center;
  margin-top: 1rem;
  font-family: Rajdhani, sans-serif;
  margin-bottom: 1rem;
}
.firstimg {
  box-shadow: 3px 3px 5px;
  margin-top: 2.5rem;
}
.secondimg {
  box-shadow: -3px 3px 5px;
  margin-top: 1rem;
}
.text {
  font-family: Rajdhani, sans-serif;
  font-size: 1.3rem;
  text-align: center;
  line-height: 2.5rem;
  font-weight: 500;
  color: #515151;
}
img {
  width: 200x;
  height: 150px;
  margin-left: 5px;
  margin-right: 10px;
  margin-top: 1rem;
}
.row {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.about-me {
  margin: 0;
  background-color: #ddcfb5;
  width: 60vh;
  height: 95vh;
  display: flex;
  flex-direction: column;
  /* justify-content: center; */
}
.row {
  margin: 1rem;
}
</style>
