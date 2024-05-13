<template>
    <nav>
        <ul>
            <li>
                <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/about">About</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/users">Usuarios (fetch)</NuxtLink>
            </li>
        </ul>
        <div class="user" @click="panelActive = !panelActive"><Icon name="line-md:account" size="2em" color="black"></Icon></div>
        <div class="panel" v-show="panelActive"></div>
    </nav>
</template>

<script setup>
    import { ref } from 'vue';
    const panelActive = ref(false);
</script>
  
<style lang="postcss">
    nav{
        position: relative;
    }
    ul {
        @apply flex p-4;

        li {
            @apply p-4;
        }
    }
    .user{
        position: absolute;
        right: 1%;
        top: 50%;
    }
    .panel{
        position: absolute;
        width: 200px;
        height: 200px;
        background-color: blue;
        right: 0;
    }
</style>