<!--
<VFSNavbar />
@copyright (c) 2022-2023. Kibble Game Studios Inc. All Rights Reserved.
-->

<!--
Vue App -> 2023 PG24Pedro pg24pedro@vfs.com
-->


<script setup>

    import {RouterLink} from 'vue-router'

//    import Controller from '@/plugins/controller'

//    import { useInfoStore } from '@/stores/infoStore.js'
//    import { useModelStore } from '@/stores/sampleStore.js'

                const navMenu = [
                    { path:"/", section: "Home" },
                    { path:"/about", section: "About" },
                    { path:"/info", section: "Info" },
                    { path: "/AdminView", section: "Admin View"},
                    { path: "/ChartView", section: "Chart View"},
                    { path: "/TestView", section: "Test View"},
                    { path: "/RecordEditView", section: "Record Edit View"}
                    
                ];
    



</script>
<template>

    <nav class="navbar">
        <ul class="menu">
            <li v-for="(item, i) in navMenu" :key="i">
                <RouterLink :to="item.path" class="menu-item">{{ item.section }}</RouterLink>
            </li>
        </ul>
    </nav>

</template>
<style scoped>
    /* navigation bar */
    li {
        display: inline-block;
        list-style: none;
    }

    nav {
        background: var(--medium);
        width: 100%;
    }

    nav a.router-link-exact-active {
        color: var(--color-text);
        font-weight: 700;
    }

    nav a.router-link-exact-active:hover {
        background-color: transparent;
    }

    nav a {
        display: inline-block;
        padding: 0 1rem;
        border-left: 1px solid var(--color-border);
    }

    nav a:first-of-type {
        border: 0;
    }

    .menu {
        align-content: flex-start;
        flex-direction: row;
        background: rgba(0, 0, 0, 0);
    }

    .navbar {
        /* background: #D10034; */
        justify-content: space-between;
        box-shadow: 0 4px 5px -5px #222;
    }
</style>