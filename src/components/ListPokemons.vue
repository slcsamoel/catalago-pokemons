<script setup>
    const pokemon = defineProps(["name" , "urlBaseSvg"]);

</script>

<template>
    <div class="col-4 col-md-6 col-xl-3">
            <div class="card p-2 mb-3 cardListPokemon">
                <p class="text-center">{{pokemon.name}}</p>
                <img
                 :src="pokemon.urlBaseSvg" 
                 class="card-img-top" 
                 :alt="pokemon.name"
                 height="80"   
                />
            </div>
    </div>
</template>

<style scoped>

    .cardListPokemon{
        
        background: rgb(34,193,195);
        background: linear-gradient(0deg, rgba(34,193,195,1) 12%, rgba(253,146,45,1) 85%);
        cursor: pointer;

    }
    .cardListPokemon:hover{
        background: rgb(34,193,195);
        background: linear-gradient(0deg, rgba(34,193,195,0.7) 20%, rgba(253,146,45,0.1) 85%);
    } 
    .cardListPokemon img:hover{
            padding: .2rem;
    }


    

</style>