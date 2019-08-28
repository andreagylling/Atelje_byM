<template>
<div class="menu-container">
  <div class="prislista" v-html="content" id="menu"></div>
</div>
</template>

<script>
import showdown from 'showdown';

export default {
  name: 'Pricelist',
  props: {
    url: String,
    required: true,
  },
  data() {
    return {
      content: '',
    };
  },
  methods: {
    loadMenu() {
      fetch(this.url)
        .then(res => res.text())
        .then((data) => {
          const converter = new showdown.Converter({
            tables: true,
          });
          this.content = converter.makeHtml(data);
        });
    },
  },
  mounted() {
    this.loadMenu();
  },
};
</script>

<style>

.prislista {
  margin: 40px 20px;
}

.prislista table {
  width: 100%;
}

.prislista td{
  text-align: left;
}

.prislista td:nth-child(2){
  text-align: right;
}

@media screen and (min-width: 835px){
  .prislista {
  margin: 20px 20px;
}
  .prislista h3 {
    margin-bottom: 12px;
  }
}
</style>
