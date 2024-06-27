<template>
  <div id="container">
    <div id="content">
      <div id="description">
        <p>
          “Moddy Character NFT”<br />
          The image is a high-quality digital painting with a resolution of
          3000x2000 pixels and is optimized for the web.
        </p>
        <span class="price">$101,593</span>
      </div>
      <div class="image">
        <img src="../assets/Rectangle 8.png" alt="Moddy Character NFT" />
      </div>
    </div>
    <div class="navigate">
      <button @click="navigateToNext"><img src="../assets/Frame 36.png" alt="navigate"></button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Root_1',
  methods: {
    navigateToNext() {
      // Logic for navigating to the next item
    },
  }
}
</script>

<style scoped>
#container {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #000;
  color: #fff;
  font-family: Arial, sans-serif;
  padding: 20px;
  border-bottom: 1rem solid;
  border-bottom-color: #816797;
}

#content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

#description {
  flex: 1;
  padding: 20px;
}

#description p {
  font-size: 1.2em;
  line-height: 1.5;
}

.price {
  font-size: 1.5em;
  color: #ff00ff;
  font-weight: bold;
}

.image {
  flex: 1;
  text-align: center;
}

.image img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
}

.navigate {
  margin-top: 20px;
}

.navigate button {
  background: none;
  border: none;
  cursor: pointer;
}

.navigate button img {
  width: 50px;
  height: 50px;
}
</style>