<template>
    <header class="bg-slate-500 w-screen h-16 flex items-center justify-center space-x-2">
        <input type="text"
        v-model="pokemonID"
        placeholder="Digite o nome ou ID"
        class="border rounded-xl p-2"
        
        >
        <button 
        class="bg-violet-600 rounded p-2 text-white"
        @click="searchPokemon"
        >
        Buscar
        </button>
    </header>
  
    <main class="w-screen h-auto flex justify-center mt-10">
       <div  v-if="Object.entries(pokemonData).length > 0">
        <PokemonCard :pokemon="pokemonData"/>
        <!-- <img :src="`https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/home/${pokemonData.id}.png`" :alt="pokemonData.name">
        <h1>{{ pokemonData.name }}</h1> -->
       </div>
    </main>
    
</template>

<script>

import { pokeapi } from '@/api/pokeapi';

export default {
  name: 'App',

  data () {
    return {
      pokemonData: {},
      pokemonID: '',
    }
  },
  methods: {
    async searchPokemon () {
      try {
        const pokemonToFind = await fetch(`${pokeapi}/${(this.pokemonID).toLocaleLowerCase()}`)
        const pokemon = await pokemonToFind.json()
        const gen = 'generation-iv'
        this.pokemonID = ''
        this.pokemonData = pokemon
        console.log(pokemon);
        return pokemon
      } catch (error) {
        alert('Pokemon was not found')
      }
    }
  }
}
</script>

<style lang="scss" scoped>

</style>