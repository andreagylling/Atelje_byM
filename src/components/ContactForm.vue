<template>
  <div class="contact-form-container">
    <h3 class="form-title">Kontakt</h3>
    <div class="input-div">
      <!-- <p class="form-section_title">Namn:</p> -->
      <input type="text" placeholder="Namn" class="input-field name_input">
    </div>
    <div class="input-div">
      <!-- <p class="form-section_title">E-post:</p> -->
      <input type="email" placeholder="E-post" class="input-field email_input">
    </div>
    <div class="input-div">
      <!-- <p class="form-section_title">Meddelande:</p> -->
      <textarea type="text" placeholder="Meddelande" class="input-field message_input"></textarea>
    </div>
    <button class="send-button" type="submit">Skicka</button>
  </div>
</template>

<script>
export default {
  name: 'ContactForm',
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Josefin+Sans&display=swap');

.form-title {
  text-align: left;
  margin-left: 50px;
  margin-bottom: 30px;
  letter-spacing: 2px;
}
.contact-form-container {
  margin-top: 60px;
  margin-bottom: 50px;
}

.input-field {
  border: 1px solid #c7bbb8;
  box-shadow: 2px 2px 2px #888888;
  height: 20px;
  width: 300px;
  font-family: 'Josefin Sans', sans-serif;
  font-size: 16px;
  padding: 10px;
  text-align: left;
}

.input-div {
  margin-bottom: 20px;
}

.message_input {
  height: 200px;
  text-align: left;
  line-height: 20px;
}

button {
  margin-top: 10px;
  background-color: #c7bbb8;
  color: white;
  padding: 15px 20px;
  text-transform: uppercase;
  font-size: 12px;
  font-weight: bold;
  letter-spacing: 1px;
  border: 1px solid #c7bbb8;
  border-radius: 3px;
}

@media screen and (min-width: 768px) {

.contact-form-container{
  margin-top: 20px;
}

}
</style>
