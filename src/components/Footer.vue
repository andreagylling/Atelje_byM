<template>
  <div class="main-div">
    <div class="footer-div">
      <p>Copyright © 2019 | Ateljé by M</p>
      <p>070 123 45 67 | contact@contact.com</p>
      <p>Ateljégatan 1, Frisörstaden</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>

.footer-div {
  margin-top: 20px;
  width: 100%;
  padding: 20px 0px;
  background-color: #c7bbb8;
}

p {
  font-size: 10px;
}

@media screen and (min-width: 768px){
  p {
    font-size: 12px;
    display: inline;
    margin-right: 20px;
  }
}

</style>
