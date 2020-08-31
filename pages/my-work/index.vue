<template>
  <div class="container">
    <div class="mywork">
      <div v-for="modal of picturesArray" :key="modal.id" :class="modal.type">
        <div class="picture">
          <div class="title">
            {{ modal.text }}
          </div>

          <img :class="modal.shape" :src="modal.link" alt="" />
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="statement">© Made by Pandaa Dev</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      picturesArray: [
        {
          id: 1,
          text:
            "“The books of poetry are the books that engage our soul, something better than education.”",
          link:
            "/wasif_hdr_61062781_1175050749333220_3903940635645095362_n.jpg",
          shape: "rectangle",
          type: "first"
        },
        {
          id: 2,
          text:
            "'The ruthless city life where everyone does anything to survive'",
          link:
            "/wasif_hdr_114827566_155780912773286_7914290580011936880_n.jpg",
          shape: "rectangle",
          type: "second"
        },
        {
          id: 3,
          text:
            "“These cold mornings are when i look around for a purpose, for a driving force”",
          link: "/wasif_hdr_26073021_745422752318804_6480440140186517504_n.jpg",
          shape: "rectangle",
          type: "second"
        },
        {
          id: 4,
          text: "“Teenage depression”",
          link: "/wasif_hdr_29417837_214842339268582_3262218761586868224_n.jpg",
          shape: "rectangle",
          type: "second"
        },
        {
          id: 5,
          text: "“Citylights”",
          link: "/wasif_hdr_30591122_2065792150310999_291355394356281344_n.jpg",
          shape: "rectangle",
          type: "second"
        },
        {
          id: 6,
          text: "“Stairs are deep”",
          link: "/wasif_hdr_62468708_444961206054359_302644480941042453_n.jpg",
          shape: "rectangle-straight",
          type: "second"
        },
        {
          id: 7,
          text: "“Books in 2020”",
          link: "/wasif_hdr_69575672_397908547594824_3043113371526501140_n.jpg",
          shape: "rectangle-straight",
          type: "second"
        },
        {
          id: 8,
          text: "“Books in 2020”",
          link: "/wasif_hdr_69575672_397908547594824_3043113371526501140_n.jpg",
          shape: "rectangle-straight",
          type: "second"
        },
        {
          id: 9,
          text: "“Cool stuff”",
          link: "wasif_hdr_71344060_2429033913845595_4389317971456172449_n.jpg",
          shape: "rectangle-straight",
          type: "second"
        },
        {
          id: 10,
          text: "“2020 in a nutshell”",
          link: "wasif_hdr_96826636_711087389652892_3108139363517539633_n.jpg",
          shape: "rectangle-straight",
          type: "second"
        }
      ]
    };
  },

};
</script>

<style>
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
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}
.title {
  text-align: center;
  margin-bottom: 1rem;
  font-family: Rajdhani, sans-serif;
  font-size: 1rem;
  font-weight: 600;
  margin-right: 1rem;
  margin-left: 1rem;
}
.second {
  margin-top: 1rem;
}
.rectangle-straight {
  height: 230px;
  width: 150px;
}
.rectangle {
  height: 150px;
  width: 70%;
  box-shadow: 1px 3.5px 5px;
}
.picture {
  height: 300px;
  width: 100%;
  background-color: #eae0cd;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.container {
  width: auto;
  height: auto;
}
</style>
