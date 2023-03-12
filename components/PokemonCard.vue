<template>
    <div class="border border-violet-900 rounded-3xl grid grid-cols-1 w-60 p-4">
        <div class="flex items-center justify-center border"
        >
            <img 
                :src="`https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/home/${pokemon.id}.png`" :alt="pokemon.name"
                class="w-40"
            >
        </div>
        <div class="flex flex-col items-center">
            <h1 class="capitalize font-bold "> {{ pokemon.name }} #{{ pokemon.id }}</h1>
            <div class="flex space-x-2">
                <ul v-for="(type,index) in pokemon.types">
                <li 
                :key="index"
                :class="type.type.name"
                class="rounded px-2 text-center uppercase font-semibold  text-slate-100"
                >{{ type.type.name }}</li>
            </ul>
            </div>
            <div class="flex flex-col">
                <ul v-for="(stat,index) in pokemon.stats">
                <li 
                :key="index"
                class="capitalize"
                >{{ stat.stat.name }} - {{ stat.base_stat }}</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script setup>

const {data:pokemon} = defineProps(['pokemon'])


</script>

<style lang="scss" scoped>

@import '@/assets/pokemonsTypes.scss';

.normal {
  background-color: $normal
}
.fire {
  background-color: $fire
}
.water {
  background-color: $water
}
.grass {
  background-color: $grass
}
.electric {
  background-color: $electric
}
.ice {
  background-color: $ice
}
.fighting {
  background-color: $fighting
}
.poison {
  background-color: $poison
}
.ground {
  background-color: $ground
}
.flying {
  background-color: $flying
}
.psychic {
  background-color: $psychic
}
.bug {
  background-color: $bug
}
.rock {
  background-color: $rock
}
.ghost {
  background-color: $ghost
}
.dark {
  background-color: $dark
}
.dragon {
  background-color: $dragon
}
.steel {
  background-color: $steel
}
.fairy {
  background-color: $fairy
}

</style>