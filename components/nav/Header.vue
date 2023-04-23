<template>
    <div class="nav item2">
        <span>
            <NuxtLink class="link" to="/">Home</NuxtLink>
        </span>
        <span>
            <NuxtLink class="link" to="/aboutus">AboutUs</NuxtLink>
        </span>
        <span>
            <NuxtLink class="link" to="/nasa">Nasa</NuxtLink>
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
    justify-content: center;
    align-items: center;
    max-height: 50px;
    min-height: 50px;
    background: lightgoldenrodyellow;
    border-bottom: 2px solid black;
}

.item2 {
    display: flex;
    width: 100%;

}

.item2 .link{
    margin-right: 10px;
    font-weight: bold;
    font-size: 24px;
    color: #333;
    padding: 50px;
    text-decoration: none;
}

</style>