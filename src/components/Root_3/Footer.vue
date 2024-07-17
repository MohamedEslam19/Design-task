<template>
  <div class="subscribe">
    <h3>Join our weekly digest!</h3>
    <p>Get exclusive promotions & updates straight to your inbox.</p>
    <form @submit.prevent="subscribe">
      <input
        type="email"
        v-model="email"
        placeholder="Enter your email"
        aria-label="Email address"
        required
      />
      <button type="submit" class="btn btn-primary">Subscribe</button>
    </form>
    <button class="btn btn-secondary mt-3">Create Free Store</button>
  </div>
  <footer class="footer">
    <div class="container">
      <div class="row">
        <div
          class="col-md-3"
          v-for="section in footerSections"
          :key="section.title"
        >
          <h5>{{ section.title }}</h5>
          <ul class="list-unstyled">
            <li v-for="link in section.links" :key="link.text">
              <a :href="link.url">{{ link.text }}</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="text-center mt-4">
        <p>The Leading No-code NFT Marketplace Solution</p>
        <div class="social-icons">
          <a href="#" aria-label="Twitter"
            ><img src="../../assets/icon_twitter.png" alt="Twitter"
          /></a>
          <a href="#" aria-label="Facebook"
            ><img src="../../assets/icon_facebook.png" alt="Facebook"
          /></a>
          <a href="#" aria-label="Instagram"
            ><img src="../../assets/icon_instagram.png" alt="Instagram"
          /></a>
          <a href="#" aria-label="LinkedIn"
            ><img src="../../assets/icon_linkedin.png" alt="LinkedIn"
          /></a>
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
  name: "Footer_",
  data() {
    return {
      email: "",
      footerSections: [
        {
          title: "FEATURES",
          links: [
            { text: "Build Store", url: "#" },
            { text: "Sell NFT", url: "#" },
            { text: "Grow Business", url: "#" },
          ],
        },
        {
          title: "SERVICES",
          links: [
            { text: "Concierge", url: "#" },
            { text: "Customization", url: "#" },
          ],
        },
        {
          title: "PRODUCT",
          links: [
            { text: "About Us", url: "#" },
            { text: "Whitepaper", url: "#" },
            { text: "$N1 Token", url: "#" },
            { text: "Directory", url: "#" },
          ],
        },
        {
          title: "RESOURCES",
          links: [
            { text: "Help Center", url: "#" },
            { text: "NFTify Branding", url: "#" },
            { text: "Success Stories", url: "#" },
            { text: "Video Tutorials", url: "#" },
            { text: "Contact Support", url: "#" },
          ],
        },
      ],
    };
  },
  methods: {
    subscribe() {
      // Implement subscription logic here
      alert(`Subscribed with email: ${this.email}`);
    },
  },
};
</script>

<style scoped>
:root {
  --primary-color: #816797;
  --secondary-color: #4b0082;
  --text-color: #fff;
}

.subscribe {
  background: var(--primary-color);
  color: var(--text-color);
  padding: 40px 0;
  text-align: center;
}

.subscribe input[type="email"] {
  width: 50%;
  padding: 10px;
  margin: 20px 0;
}

.footer {
  background-color: var(--secondary-color);
  padding: 40px 0;
  color: white;
}

.footer a {
  color: var(--text-color);
  text-decoration: none;
}

.footer a:hover {
  text-decoration: underline;
}

.social-icons a {
  margin: 0 10px;
}

@media (max-width: 576px) {
  .subscribe input[type="email"] {
    width: 80%;
  }
}
</style>
