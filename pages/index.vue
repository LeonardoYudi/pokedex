<template>
  <div class="grid grid-cols-2 h-full">
    <div class="flex flex-col justify-center items-start px-12">
      <h1 class="text-neutral-200 text-5xl font-semibold mb-4 ">Bem-Vindo a <br> Pokedex</h1>
      <p class="text-neutral-200">A Pokédex contém muitas informações sobre todas as criaturas Pokémon de toda a série de jogos. Nas páginas da lista principal, você pode ver as várias estatísticas de cada Pokémon. Clique no nome de um Pokémon para ver uma página detalhada com dados Pokédex, descrições de jogos anteriores, sprites, evoluções, movimentos e muito mais!</p>
    </div>
    <div class="flex justify-center items-center">
      <img src="@/public/pikachu.png" alt="">
    </div>
  </div>
</template>

<script>
  export default {
      setup(){
        definePageMeta({
            layout:'default'
        })
        useHead({
          title: 'Pokedex | Home'
        })
      }
  }
</script>

<style lang="scss" scoped>

</style>