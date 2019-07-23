<template>
  <div class="hours-div">
    <h3 class="hours-title">Öppettider</h3>
    <div v-html="content" class="hours-table"></div>
  </div>
</template>

<script>
import showdown from 'showdown';

export default {
  name: 'Hours',
  data() {
    return {
      content: '',
    };
  },
  methods: {
    loadHours() {
      fetch('Atelje_byM/content/oppettider.md')
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
    this.loadHours();
  },
};
</script>


<style>

  .hours-div {
    border: 1px dotted black;
    padding: 10px 0px;
    margin: 60px 15px 0px 15px;
  }
  .hours-table {
    display: grid;
    text-align: left;
    justify-content: center;
  }

  .hours-table td{
    padding: 10px 40px;
  }

  .hours-table td:nth-child(2){
    text-align: right;
  }

  .hours-title {
    letter-spacing: 2px;
  }

  @media screen and (min-width: 835px){
    .hours-title{
      text-align: left;
      margin-left: 60px
    }

    .hours-div {
      margin-top: 12px;
      border: none;
    }
  }

</style>
