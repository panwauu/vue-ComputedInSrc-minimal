<template>
    <img alt="Vue logo" :src="require('../assets/logo.png')" />

    <!-- This works with serve and with build -->
    <img alt="Vue logo" :src="require('../assets/' + imageSrc)" />

    <!-- This works with serve not with build -> ReferenceError: _unref is not defined -->
    <img alt="Vue logo" :src="require(`../assets/${imageSrc}`)" />
</template>

<script setup lang="ts">
import { computed } from 'vue';
const imageSrc = computed(() => { return 'logo.png' })
</script>