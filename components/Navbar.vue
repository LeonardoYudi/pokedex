<template>
        <nav class="space-x-12 text-neutral-200 font-semibold uppercase w-full h-full flex justify-center items-center border-b-[1px] border-[#373737]">
            <nuxt-link to="/">Home</nuxt-link>
            <nuxt-link to="/dashboard">Dashboard</nuxt-link>
            <nuxt-link to="/myList">My List</nuxt-link>
            <nuxt-link to="/about">About</nuxt-link>
        </nav>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
    .router-link-exact-active{
        color:aquamarine;
    }
</style>