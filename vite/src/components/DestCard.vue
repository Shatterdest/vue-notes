<template>
    <div>
<h2>{{ Destination.name }}</h2>
<img :src="Destination.img" alt="" />
<h3>{{ clicked }}</h3>
<button @click="increment">click me</button>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const props = defineProps({
    Destination:Object,
})

const clicked = ref(0)
function increment() {
    clicked.value++
}
</script>

<style lang="css" scoped>
img {
    width: 300px;
    height: 350px;
    object-fit: cover;
}
</style>