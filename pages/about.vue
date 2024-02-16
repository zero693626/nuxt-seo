<script setup>
useHead({
        title: '關於我們',
        meta: [
                { name: 'description', content: '這是關於我們' }
        ],
        bodyAttrs: {
                class: 'test'
        },
        script: [{ innerHTML: 'console.log(\'Hello world\')' }]
})
</script>
<template>
        <h1>關於我們</h1>
</template>
<style></style>