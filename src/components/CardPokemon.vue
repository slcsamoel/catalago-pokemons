
<script setup>
const pokemon = defineProps(['name','xp' , 'height' , 'img' , 'loading'])


</script>

<template>
        <div :class="loading ? '' :'animate__animated animate__flipInX'" class="card cardPokemonSelected">
            
            <img
               v-if="pokemon.name"  
               :src="pokemon.img" 
               height="250"
               class="card-img-top pt-2"
               :alt="pokemon.name"
             >

             <img 
               v-else 
               src="../assets/egg_pokemon.svg" 
               height="250"
               class="card-img-top pt-2"
               :alt="pokemon.name"
             >

            <div class="card-body">
                <h5 class="card-title text-center">{{ pokemon.name || '???' }}</h5>
                <hr>
                <div class="row">
                    <section class="col">
                           <strong>XP:</strong> 
                           <span>{{ pokemon.xp }}</span>
                    </section>
                    <section class="col">
                            <strong>Altura:</strong> 
                            <span>{{ pokemon.height }}</span>
                    </section>
                </div>        

            </div>
        </div>
</template>


<style scoped>

 .cardPokemonSelected{
        height: 75vh;
        background: rgb(12, 77, 199);
        background: linear-gradient(0deg, rgb(82, 127, 248) 12%, rgb(216, 238, 24) 85%);

 }


</style>