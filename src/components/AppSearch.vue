<script>

import axios from 'axios';
import { store } from "../store.js";

export default {
    name: 'AppSearch',

    data() {
        return {
            store,
            archetypes: [],
    };
    },
    methods: {
        getArchetypesFromApi() {
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((response) => {
                console.log(response.data);
                this.archetypes = response.data;
            }); 
        }
    }, 
    mounted() {
        this.getArchetypesFromApi();
    },
}


</script>

<template>
    
    <div class="app-search">
        
        <div class="container">
            <select v-model="store.selectedArchetypes" @change="$emit('searchPerformed')" >
                
                <option value=""></option>
                <option v-for="archetype in archetypes" :value="archetype.archetype_name">{{ archetype.archetype_name }}</option>
            </select>
        </div>
    </div>
    
</template>

<style scoped lang="scss">
@use '../style/generic';




</style>