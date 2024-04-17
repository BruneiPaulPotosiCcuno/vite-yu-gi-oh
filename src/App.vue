<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import CardList from './components/CardList.vue';
import AppSearch from './components/AppSearch.vue';

export default {
  components: {
    AppHeader,
    CardList,
    AppSearch,
  },
data() {
  return {
    store
  };
 },
  
 methods: {
  getCharacterFromApi() {

    const queryParams = {
      num: 20,
      offset: 0,
    };

    
    
    if(store.selectedArchetypes !== '') {
      queryParams.archetype = store.selectedArchetypes; 
    }

    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
      params: queryParams
    })
    .then((response) => {
      
      store.characters = response.data;
      
    });
  }
  
 },

 mounted() {
  this.getCharacterFromApi();
  
 }
}
</script>

<template>
    <AppHeader @searchPerformed="getCharacterFromApi"></AppHeader>
    <main>
        <AppSearch ></AppSearch>
        <CardList></CardList>
    </main>
</template>

<style lang="scss">
@use './style/generic.scss';
</style> 