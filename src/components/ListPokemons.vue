<script setup>
    const pokemon = defineProps(["name" , "urlBaseSvg"]);

</script>

<template>
    <div class="col-4">
            <div class="card p-2 mb-3">
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

</style>