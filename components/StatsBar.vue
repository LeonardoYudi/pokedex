<template>
    <div class="w-full h-full grid grid-cols-4  border-t-[1px] border-[#373737]">
        <ButtonStats>Description</ButtonStats>
        <ButtonStats>Catching</ButtonStats>
        <ButtonStats>Weather Effects</ButtonStats>
        <ButtonStats>Capable Moves</ButtonStats>
    </div>
</template>

<script>
import ButtonStats from '~~/components/ButtonStats.vue'
    export default {
        components:{
            ButtonStats
        }
    }
</script>

<style lang="scss" scoped>

</style>