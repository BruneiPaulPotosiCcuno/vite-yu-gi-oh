<script>
import { store } from './store.js'
import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'
export default {
  components: {
    AppHeader,
    CardList
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
@use './style/generic.scss'
</style> 