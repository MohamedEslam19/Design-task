<template>
    <div id="nftCarousel" class="carousel slide" data-ride="carousel">
        <div class="carousel-inner">
            <div class="carousel-item" :class="{ active: index === 0 }" v-for="(item, index) in items" :key="index">
                <img :src="item.image" :alt="item.title">
                <div class="carousel-caption">
                    <h5>{{ item.title }}</h5>
                    <p class="floor">Floor: {{ item.floor }} ETH</p>
                </div>
            </div>
        </div>
        <a class="carousel-control-prev" href="#nftCarousel" role="button" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#nftCarousel" role="button" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
        </a>
    </div>
</template>

<script>
import image1 from '../../assets/image_1.png';
import image2 from '../../assets/image_2.png';
import image3 from '../../assets/image_3.png';
import image4 from '../../assets/image_4.png';

export default {
    name: 'NftCarousel',
    data() {
        return {
            items: [
                { title: "XO Girls NFT Collection", floor: 0.07, image: image1 },
                { title: "Game character 3d Collection", floor: 0.05, image: image2 },
                { title: "Monkey Collections", floor: 0.01, image: image3 },
                { title: "PROJECT NFT cub", floor: 0.07, image: image4 }
            ]
        }
    }
}
</script>

<style>
.carousel-item img {
    height: 25%;
    width: 25%;
}

.carousel-item .floor {
    margin-top: 10px;
}
</style>
