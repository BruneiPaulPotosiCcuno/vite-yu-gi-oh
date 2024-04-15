<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <header>
        <h1>YU-GI-OH Api</h1>
    </header>
</template>

<style scoped lang="scss">
    header{
        display: flex;
        font-size: 20px;
        background-color: white;
        height: 80px;
        
        h1{
            display: flex;
            align-items: center;
            position: relative;
            left: 90px;
        }
    }
</style>