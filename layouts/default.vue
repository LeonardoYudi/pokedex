<template>
   <div class="grid grid-template-columns grid-template-rows bg-[#313131] h-screen w-screen">
        <div class="flex justify-center items-center border-r-[1px] border-b-[1px] border-[#373737]"><img src="@/public/pkbal.png" alt="" class="h-12 w-12"></div>
        <Navbar></Navbar>
        <div class="flex justify-center items-center border-l-[1px] border-b-[1px] border-[#373737]"><img src="@/public/pkbal.png" alt="" class="h-12 w-12"></div>
        
        <div class="flex items-center justify-center border-r-[1px] border-[#373737]"></div>
        <div class=""><slot></slot></div>
        <div class="flex items-center justify-center border-l-[1px] border-[#373737]"></div>

        <div class="flex justify-center items-center border-r-[1px] border-t-[1px] border-[#373737]"><img src="@/public/pkbal.png" alt="" class="h-12 w-12"></div>
        <FooterBar></FooterBar>
        <div class="flex justify-center items-center border-l-[1px] border-t-[1px] border-[#373737]"><img src="@/public/pkbal.png" alt="" class="h-12 w-12"></div>
   </div>

</template>

<script>

import { defineComponent } from 'vue';

export default defineComponent({
    setup () {

        return {}
    }
})
</script>

<style scoped>
    .grid{
        display: grid;
    }

    .grid-template-columns{
        grid-template-columns: 80px auto 80px;
    }

    .grid-template-rows{
        grid-template-rows: 80px auto 80px;
    }
    

</style>