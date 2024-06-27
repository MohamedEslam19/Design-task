<template>
    <div class="subscribe">
        <h3>Join our weekly digest!</h3>
        <p>Get exclusive promotions & updates straight to your inbox.</p>
        <form>
            <input type="email" placeholder="Enter your email">
            <button type="submit" class="btn btn-primary">Subscribe</button>
        </form>
        <button class="btn btn-secondary mt-3">Create Free Store</button>
    </div>
</template>

<script>
export default {
    name: 'Subscribe_'
}
</script>

<style scoped>
.subscribe {
    background: #816797;
    padding: 40px 0;
    text-align: center;
}

.subscribe input[type="email"] {
    width: 50%;
    padding: 10px;
    margin: 20px 0;
}
</style>
