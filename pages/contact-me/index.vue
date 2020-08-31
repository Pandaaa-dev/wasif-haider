<template>
  <div class="container">
    <div class="contact-me">
      <div class="title">Contact me</div>
      <section class="form">
        <form class="contact-form">
          <section class="areas name">
            <label for="Name">Name:</label>
            <input type="text" />
          </section>
          <section class="areas subject">
            <label for="Subject">Subject:</label>
            <input type="text" />
          </section>
          <section class="areas message">
            <label for="Message">Message:</label>
            <textarea name="message" id="" cols="30" rows="10"></textarea>
          </section>
          <section class="button">
            <div class="button-submit" @click="$router.push('/')" >Submit</div>
          </section>
        </form>
      </section>
    </div>

    <div class="footer">
      <div class="statement">© Made by Pandaa Dev</div>
    </div>
  </div>
</template>

<script>
import contactVue from '../../layouts/contact.vue';
export default { 
  layout: "contact"
};
</script>

<style>
.button {
  margin-top: 1rem;
  border: none;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
  padding-left: 1rem;
  padding-right: 1rem;
  border-radius: 1rem;
  background-color: #cab286;
  font-family: Rajdhani, sans-serif;
  font-weight: 700;
}
.button:hover {
  opacity: 0.5;
}
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
input {
  border: none;
  border-radius: 1rem;
  height: 1.3rem;
}
textarea {
  border: none;
  border-radius: 1rem;
}
.title {
  font-family: Rajdhani, sans-serif;
  font-size: 3rem;
  font-weight: 600;
}
.areas {
  margin: 1rem;
}
.message {
  display: flex;
  flex-direction: column;
}
.contact-form {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  margin-top: 2rem;
}
.contact-me {
  background-color: #ddcfb5;
  height: 90vh;
  width: 60vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: Rajdhani, sans-serif;
  font-size: 1.2rem;
}
label {
  font-weight: 500;
}

</style>
