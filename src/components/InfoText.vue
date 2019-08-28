<template>
  <div v-html="content" class="about-container"></div>
</template>

<script>
import showdown from 'showdown';

export default {
  name: 'InfoText',
  data() {
    return {
      content: '',
    };
  },
  methods: {
    loadAbout() {
      fetch('Atelje_byM/content/about.md')
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
    this.loadAbout();
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=DM+Serif+Text&display=swap');
@import url('https://fonts.googleapis.com/css?family=Merriweather&display=swap');
@import url('https://fonts.googleapis.com/css?family=Playfair+Display&display=swap');

.about-container {
  margin: 100px 40px 100px 40px;
  border-top: 1px solid black;
}

.about-container p {
  font-family: 'DM Serif', serif;
  letter-spacing: 0.5px;
  line-height: 35px;
  font-size: 20px;
}

@media screen and (min-width: 768px){
  .about-container {
    margin-top: 0px;
    margin-bottom: 0px;
  }

  .about-container p {
    font-size: 18px;
    line-height: 30px;

  }
}

@media screen and (min-width: 992px){
  .about-container p {
    font-size: 20px;
    line-height: 35px;
  }
}
</style>
