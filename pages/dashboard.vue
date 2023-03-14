<template>
    <div class="flex justify-center items-center">
        <h1 class="text-[36px] text-sky-50">Em desenvolvimento</h1>
    </div>
</template>

<script>
export default {
   
    setup () {

        definePageMeta({
            layout:'pokemon-data'
        })
        useHead({
            title: 'Pokedex | Dashboard'
        })
        return {}
    }
}
</script>

<style lang="scss" scoped>

</style>