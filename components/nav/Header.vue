<template>
    <div class="nav item2">
        <span>
            <NuxtLink class="link" to="/">Home</NuxtLink>
        </span>
        <span>
            <NuxtLink class="link" to="/aboutus">AboutUs</NuxtLink>
        </span>
    </div>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped>
.nav {
    display: flex;
    /* flex-direction: column; */
    height: 100%;
    width: 100%;
    max-height: 200;
    min-height: 200;
    background: lightgoldenrodyellow;
}

.item2 {
    display: block;
    width: 100%;
    text-align: right;
}

.item2 .link{
    margin-right: 10px;
    font-weight: bold;
    font-size: 22px;
    color: #333;
    text-decoration: none;
}

</style>