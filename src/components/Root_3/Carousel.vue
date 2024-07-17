<template>
  <div class="container text-center my-3">
    <h2 class="head">Collections</h2>
    <div class="row mx-auto my-auto justify-content-center">
      <div id="recipeCarousel" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner" role="listbox">
          <div
            v-for="(item, index) in items"
            :key="index"
            :class="['carousel-item', { active: index === 0 }]"
          >
            <div class="col-md-3">
              <div class="card">
                <div class="card-img">
                  <img :src="item.image" class="img-fluid" />
                </div>
                <div class="card-img-overlay">
                  {{ item.title }}<br />
                  Floor:{{ item.floor }}
                </div>
              </div>
            </div>
          </div>
        </div>
        <a
          class="carousel-control-prev bg-transparent justify-content-lg-start"
          href="#recipeCarousel"
          role="button"
          data-bs-slide="prev"
        >
          <span class="prev-icon" aria-hidden="true"
            ><img :src="prevBtn" alt="previous"
          /></span>
        </a>
        <a
          class="carousel-control-next bg-transparent justify-content-end"
          href="#recipeCarousel"
          role="button"
          data-bs-slide="next"
        >
          <span class="next-icon" aria-hidden="true"
            ><img :src="nextBtn" alt="next"
          /></span>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import image1 from "../../assets/image_1.png";
import image2 from "../../assets/image_2.png";
import image3 from "../../assets/image_3.png";
import image4 from "../../assets/image_4.png";
import prevBtn from "../../assets/prev_btn.png";
import nextBtn from "../../assets/next_btn.png";

export default {
  name: "Carousel_",
  data() {
    return {
      items: [
        { title: "XO Girls NFT Collection", floor: 0.07, image: image1 },
        { title: "Game character 3d Collection", floor: 0.05, image: image2 },
        { title: "Monkey Collections", floor: 0.01, image: image3 },
        { title: "PROJECT NFT cub", floor: 0.07, image: image4 },
      ],
      prevBtn,
      nextBtn,
    };
  },
  mounted() {
    let items = this.$el.querySelectorAll(".carousel .carousel-item");
    items.forEach((el) => {
      const minPerSlide = 4;
      let next = el.nextElementSibling;
      for (let i = 1; i < minPerSlide; i++) {
        if (!next) {
          next = items[0];
        }
        let cloneChild = next.cloneNode(true);
        el.appendChild(cloneChild.children[0]);
        next = next.nextElementSibling;
      }
    });
  },
};
</script>

<style scoped>
.head {
  text-align: left;
  justify-content: baseline;
  color: white;
  font-weight: bold;
}
@media (max-width: 767px) {
  .carousel-inner .carousel-item > div {
    display: none;
  }
  .carousel-inner .carousel-item > div:first-child {
    display: block;
  }
}

.card-img-overlay {
  background: #000000bf;
  opacity: 80%;
  font-family: Poppins;
  font-size: 16px;
  display: block;
  justify-content: center;
  margin-top: 65%;
  color: white;
  font-weight: bold;
}

.carousel-inner .carousel-item.active,
.carousel-inner .carousel-item-next,
.carousel-inner .carousel-item-prev {
  display: flex;
}

/* medium and up screens */
@media (min-width: 768px) {
  .carousel-inner .carousel-item-end.active,
  .carousel-inner .carousel-item-next {
    transform: translateX(25%);
  }
  .carousel-inner .carousel-item-start.active,
  .carousel-inner .carousel-item-prev {
    transform: translateX(-25%);
  }
}

.carousel-inner .carousel-item-end,
.carousel-inner .carousel-item-start {
  transform: translateX(0);
}
</style>
