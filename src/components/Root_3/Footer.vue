<template>
    <footer class="footer">
        <div class="container">
            <div class="row">
                <div class="col-md-3" v-for="section in footerSections" :key="section.title">
                    <h5>{{ section.title }}</h5>
                    <ul class="list-unstyled">
                        <li v-for="link in section.links" :key="link"><a href="#">{{ link }}</a></li>
                    </ul>
                </div>
            </div>
            <div class="text-center mt-4">
                <p>The Leading No-code NFT Marketplace Solution</p>
                <div>
                    <a href="#"><img src="../../assets/icon _twitter_.png" alt="Twitter"></a>
                    <a href="#"><img src="../../assets/icon _facebook outline_.png" alt="Facebook"></a>
                    <a href="#"><img src="../../assets/icon _instagram icon_.png" alt="Instagram"></a>
                    <a href="#"><img src="../../assets/icon _linkedin_.png" alt="LinkedIn"></a>
                </div>
            </div>
            <div class="text-center mt-4">
                <p>&copy; Copyright NFTify Network. All Rights Reserved.</p>
                <p><a href="#">Terms of Service</a> | <a href="#">Privacy Policy</a></p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer_',
    data() {
        return {
            footerSections: [
                { title: "FEATURES", links: ["Build Store", "Sell NFT", "Grow Business"] },
                { title: "SERVICES", links: ["Concierge", "Customization"] },
                { title: "PRODUCT", links: ["About Us", "Whitepaper", "$N1 Token", "Directory"] },
                { title: "RESOURCES", links: ["Help Center", "NFTify Branding", "Success Stories", "Video Tutorials", "Contact Support"] }
            ]
        }
    }
}
</script>

<style scoped>
.footer {
    background-color: #4B0082;
    padding: 40px 0;
    color: #fff;
}

.footer a {
    color: #fff;
    text-decoration: none;
}

.footer a:hover {
    text-decoration: underline;
}
</style>
