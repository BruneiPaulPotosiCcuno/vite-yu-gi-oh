<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import CardList from './components/CardList.vue';

export default {
  components: {
    AppHeader,
    CardList,
  },
data() {
  return {
    store
  };
 },
 methods: {
  getCharacterFromApi() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
    .then((response) =>{
      
      store.characters = response.data;
      
    } );
    
  }
 },
 mounted() {
  this.getCharacterFromApi();
 }
}
</script>

<template>
    <AppHeader></AppHeader>
    <main>
        <CardList></CardList>
    </main>
</template>

<style lang="scss">
@use './style/generic.scss';
</style> 