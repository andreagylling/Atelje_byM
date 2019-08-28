<template>

    <div class="div-comp" v-bind:style="{ 'background-image': 'url(' + img + ')' }">
        <div class="text text-container">
          <p>{{text}}</p>
          <h1>{{title}}</h1>
          <a href="/#/about">{{button}}</a>
        </div>
    </div>
</template>

<script>
export default {
  name: 'MainPageContainer',
  props: {
    title: String,
    text: String,
    button: String,
    img: String,
  },
};
</script>

<style scoped lang="scss">

.div-comp{
  position: relative;
  width: 100%;
  height: 500px;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}


.text {
  color: white;
  text-decoration: none;
  font-size: 16px;
}

.text-container {
  margin: auto;
  position: absolute;
  top: 200px; left: 0; bottom: 0; right: 0;

}

a {
  text-decoration: none;
  background-color: #c7bbb8;
  color: white;
  padding: 15px 20px;
  text-transform: uppercase;
  font-size: 12px;
}

h1 {
  margin-bottom: 30px;
}

</style>
