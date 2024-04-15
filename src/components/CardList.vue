<script>
import CharacterCard from './CharacterCard.vue'
export default {
    name: 'CardList',
    components: {
        CharacterCard
    }
}
</script>

<template>
    <section class="cards-list">
        <div class="container">
            <div class="character-cards">
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                <CharacterCard></CharacterCard>
                
            </div>
        </div>
    </section>
</template>

<style>
    .cards-list{
        
        .character-cards{
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin: 50px 0;
            padding: 40px;
        }
    }

    .container{
        
        background-color: rgb(255, 255, 255);
    }
</style>