<template>
    <header>
        <img :src='logo' :alt='alt'>
    </header>
</template>

<script>
export default ({
    name: 'Header',
    data() {
        return {
            logo: '../assets/dc-logo.png',
            alt:'Logo DC'
        }
    }
})
</script>

<style scoped lang = 'scss'>
    
</style>