<!--
    usage:

<MessageOfTheDaysize="24"> Myuser message here </MessageOfTheDay>
Copyright (c) 2022-2023. Kibble Game Studios Inc. All Rights Reserved.
-->

<script setup>

    const props = defineProps({
        size:Number
    });

    let myFirstViewModelVariable = `font-size:${props.size}px`;

</script>

<template>


    <div class="bright message" style="">

        <div :style="`font-size:${props.size}px`">
        <slot></slot>

        </div>
    </div>

</template>

<style scoped>
    .bright{color: white;}
    .message{font-size:14px;}

</style>
