<template>
    <div class="h-full w-full grid grid-cols-3 grid-rows-2">
        <AbouItem>Vue / Nuxt</AbouItem>
        <AbouItem>Pokeapi</AbouItem>
        <AbouItem>Tailwind</AbouItem>
        <AbouItem>Pinia</AbouItem>
        <AbouItem>GitHub</AbouItem>
        <AbouItem>Vercel</AbouItem>
    </div>
</template>

<script>
import AbouItem from '~~/components/AbouItem.vue';

    export default {
        components:{
            AbouItem
        },
        setup(){
            definePageMeta({
            layout:'default'
            })
            useHead({
                title: 'Pokedex | About'
            })
        }
    }
</script>

<style lang="scss" scoped>

</style>