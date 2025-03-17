<template>
    <div>
        <h1>Color mode: {{ $colorMode.value }}</h1>
        <select v-model="$colorMode.preference">
            <option value="system">System</option>
            <option value="light">Light</option>
            <option value="dark">Dark</option>
        </select>
    </div>
    <NuxtLayout>
        <Nuxtpage />
    </NuxtLayout>
</template>

<script setup>
const colorMode = useColorMode();

console.log(colorMode.preference);
console.log(colorMode);
</script>

<style>
body {
    background-color: #fff;
    color: rgba(0, 0, 0, 0.8);
}

.dark-mode body {
    background-color: #091a28;
    color: #ebf4f1;
}
</style>
