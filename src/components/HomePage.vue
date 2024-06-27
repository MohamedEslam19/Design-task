<template>
    <div>
        <header>
            <div class="logo">VMeta 3</div>
            <nav>
                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#blog">Blog</a>
                <a href="#cart">Cart</a>
                <a href="#login">Login</a>
                <a href="#signup">Sign Up</a>
            </nav>
        </header>
        <section class="hero">
            <h1>Your own NFT Market place without Coding</h1>
            <p>The fastest and easiest way to fully unlock the potential of your digital assets. Create and run an
                exclusive marketplace for your NFT business today!</p>
            <div>
                <input type="email" placeholder="Enter your email..." />
                <button>Start Free</button>
            </div>
        </section>
        <footer>
            <div>Powering leading brands</div>
            <div class="brands">
                <img src="../assets/coindesk_logo.png" alt="Coindesk" />
                <a>Coindesk</a>
                <img src="../assets/heftyverse_logo.png" alt="H E F T Y V E R S E" />
                <a>H E F T Y V E R S E</a>
            </div>
        </footer>
    </div>
</template>
<script>
export default {
    name: 'HomePage'
}
</script>

<style scoped>
/* Header Styles */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 50px;
    background: #000;
}

header .logo {
    font-size: 24px;
    font-weight: bold;
}

header nav {
    display: flex;
    gap: 20px;
}

header nav a {
    color: white;
    text-decoration: none;
    font-size: 18px;
}

header nav a:hover {
    text-decoration: underline;
}

/* Hero Section Styles */
.hero {
    height: 100vh;
    background: url('../assets/Rectangle\ 1.png') no-repeat center center/cover;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 0 20px;
}

.hero h1 {
    font-size: 48px;
    margin-bottom: 20px;
}

.hero p {
    font-size: 24px;
    margin-bottom: 30px;
}

.hero input[type="email"] {
    padding: 15px;
    font-size: 18px;
    border: none;
    border-radius: 5px;
    margin-right: 10px;
}

.hero button {
    padding: 15px 30px;
    font-size: 18px;
    border: none;
    border-radius: 5px;
    background-color: #6200EA;
    color: white;
    cursor: pointer;
}

.hero button:hover {
    background-color: #3700B3;
}

/* Footer Styles */
footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 50px;
    background: #816797;
}

footer .brands {
    display: inline-block;
    gap: 20px;
}

footer .brands img {
    height: 30px;
    margin-left: 20px;
}

footer .brands a {
    /* height: 30px; */
    font-family: Poppins;
    font-size: 15px;
    font-weight: 400;
    line-height: 37.5px;
    text-align: left;
    /* margin-left: 20px; */
}

/* Responsive Styles */
@media (max-width: 768px) {

    header,
    footer {
        flex-direction: column;
        align-items: flex-start;
    }

    .hero h1 {
        font-size: 36px;
    }

    .hero p {
        font-size: 18px;
    }
}
</style>