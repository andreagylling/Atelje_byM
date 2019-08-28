<template>
  <div class="home">
    <div class="top-div">
      <MainPageContainer title="Ateljén" text="Modern Harmoni" button="Galleri" img="Atelje_byM/img/studio1.jpg"/>
      <InfoText />
    </div>
    <div class="middle-div">
      <div class="menu-div">
        <h2 class="price-title">Prislista</h2>
        <hr>
        <Pricelist url="Atelje_byM/content/menyklipp.md" />
        <Pricelist url="Atelje_byM/content/menyfarg.md" />
        <Pricelist url="Atelje_byM/content/menyhairtalk.md" />
      </div>
      <MainPageContainer title="Inspiration" text="En ny look" button="Från Ateljén" img="Atelje_byM/img/inspo2.png"/>
    </div>
    <div class="bottom-div">
      <Hours />
      <ContactForm />
    </div>
    <Footer />
  </div>
</template>

<script>
import MainPageContainer from '@/components/MainPageContainer.vue';
import Pricelist from '@/components/Pricelist.vue';
import InfoText from '@/components/InfoText.vue';
import Hours from '@/components/Hours.vue';
import ContactForm from '@/components/ContactForm.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'home',
  components: {
    MainPageContainer,
    Pricelist,
    InfoText,
    Hours,
    ContactForm,
    Footer,
  },
};
</script>

<style>

.price-title {
  letter-spacing: 2px;
}

@media screen and (min-width: 768px) {

  .home {
    margin: 0px 30px;
  }

  .top-div {
    display: grid;
    grid-template-columns: 50% 50%;
    margin-top: 50px;
    justify-self: center;
  }

  .middle-div {
    display: grid;
    grid-template-columns: 50% 50%;
  }

  .bottom-div {
    display: grid;
    grid-template-columns: 50% 50%;
  }

  .price-title {
    margin: 30px 0px 10px 0px;
  }

  .menu-div {
    border-bottom: 1.5px dotted black;
  }
}
</style>
