<script>
export default {
    name: 'CharacterCard.vue'
}
</script>

<template>
    
    <div class="character-card">
        <div class="image">
            <img src="https://images.ygoprodeck.com/images/cards_small/91231901.jpg" alt="">
        </div>
        <h1>Nome</h1>
        <div>Species</div>
    </div>
</template>

<style scoped lang = "scss">
    .character-card {

        h1{
            color: white;
        } 

        background-color: #d48f38;
        width: calc((100% / 5) - 20px);
        text-align: center;

        img{
            width: 100%;
        }
    }
</style>