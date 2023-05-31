<script setup>

import { RouterLink, RouterView } from 'vue-router'

import VFSHeader from '@/components/Header.vue'
import VFSNavbar from '@/components/Navbar.vue'
import RCTMessageOfTheDay from '@/components/MessageOfTheDay.vue'

// todo import appInfoStore

</script>
<template>

    <header class="wrapper container columns">
        <VFSHeader title="A sample app" />
        
        <VFSNavbar />
    </header>
    <main>
        <RCTMessageOfTheDay size="23"> My Message of the day is: Hail Venom </RCTMessageOfTheDay>
        <RouterView />
    </main>

</template>
<style>

    header {
        background: #b502e2;
        flex-direction: column;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        align-items: center;
        justify-content: space-between;
        box-shadow: 0 4px 5px -5px #222;
        width: 100vw;
    }

    /* VFSHeader {
        line-height: 1.5;
        max-height: 20vh;
    } */

    @media (min-width: 1024px) {
      header {
          display: flex;
          place-items: center;
          padding-right: calc(var(--section-gap) / 2);
      }

      .logo {
          margin: 0 2rem 0 0;
      }

      header .wrapper {
          display: flex;
          place-items: flex-start;
          flex-wrap: wrap;
      }
    }
</style>
