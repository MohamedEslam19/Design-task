<template>
  <div id="root">
    <div class="HomePage">
      <HomePage />
    </div>
    <div class="page_1">
      <Root_1 />
    </div>
    <div class="page_2">
      <Root_2 />
    </div>
    <div class="page_3">
      <NftCarousel />
      <Subscribe_ />
      <Footer_ />
    </div>
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue';
import Root_1 from './components/Root_1.vue';
import Root_2 from './components/Root_2.vue';
import NftCarousel from './components/Root_3/Carousel.vue';
import Subscribe_ from './components/Root_3/Subscribe.vue';
import Footer_ from './components/Root_3/Footer.vue';

// import Root_3 from './components/Root_3/Root_3.vue';


export default {
  name: 'App',
  components: {
    HomePage,
    Root_1,
    Root_2,
    NftCarousel,
    Subscribe_,
    Footer_
  }
};
</script>

<style scoped>
#root {
  display: inline-block;
  width: 100%;
  height: 100vh;
  font-family: Arial, sans-serif;
}

.HomePage {
  min-width: 200px;
  /* padding: 20px; */
  /* background: #2c3e50; */
  color: #ecf0f1;
  /* border-right: 1px solid #34495e; */
  overflow-y: auto;
}


.page_1 {
  min-width: 200px;
  /* min-width: 700px; */
  /* flex: 1;
  padding: 20px;
  background: #ecf0f1;*/
  overflow-y: auto;
}

.page_2 {
  min-width: 200px;
  overflow-y: auto;
}

.page_3 {
  min-width: 200px;
  /* min-width: 700px; */
  /* flex: 1;
  padding: 20px;
  background: #ecf0f1;*/
  background: linear-gradient(180deg, #52057B 0%, #000000 100%);
  overflow-y: auto;
}
</style>
