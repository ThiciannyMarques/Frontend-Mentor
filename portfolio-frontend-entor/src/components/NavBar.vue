<template>
    <header >
        <nav >
            <img src="../assets/logo.svg" alt=""> 
            <div>
                <router-link> About </router-link>
                <router-link> Carrers </router-link>
                <router-link> Events </router-link>
                <router-link> Products </router-link>
                <router-link> Support </router-link>
            </div>   
        </nav>
    </header>
</template>

<script>
    export default {

    }
</script>

<style>
    nav{
        
        margin: 0px;
        background: blue;
        background-image: url('../assets/desktop/image-hero.jpg');
    }
</style>