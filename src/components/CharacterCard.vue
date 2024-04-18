<script>
export default {
    name: 'CharacterCard',
    props: {
        characterInfo: Object
    }
} 
</script>

<template>
    
    <div class="character-card">
        <div class="image">
            <img :src="characterInfo.card_images[0].image_url">
        </div>
        <h1>{{ characterInfo.name }}</h1>
        <div class="archetype">{{ characterInfo.archetype}}</div>
    </div>
</template>

<style scoped lang = "scss">
    .character-card {

        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;

        h1{
            color: white;
        } 

        background-color: #d48f38;
        width: calc((100% / 5) - 20px);
        text-align: center;

        img{
            width: 100%;
        }

        padding-bottom: 12px;

        .archetype {
        font-size: 20px;
        font-weight: 300;    
        }
        
    }
</style>