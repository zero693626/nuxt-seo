<script setup>

const { count } = useAddCount();
// const { data } = await useAsyncData('mountains', () => $fetch('https://api.nuxtjs.dev/mountains'));
const { data } = await useFetch('https://api.nuxtjs.dev/mountains');
if (process.client) {
        console.log(window);
}

onMounted(() => {
        console.log(window);
})

useHead({
  title: '首頁',
  meta: [
    { name: 'description', content: '這是首頁' }
  ],
  bodyAttrs: {
    class: 'test'
  },
  script: [ { innerHTML: 'console.log(\'Hello world\')' } ]
})


</script>
<template>
        <h1>首頁</h1>
        <Card />
        <Box />
        <!-- {{ count }} -->
        <ul>
                <li v-for="item in data">
                        {{ item }}
                </li>
        </ul>
</template>
<style></style>