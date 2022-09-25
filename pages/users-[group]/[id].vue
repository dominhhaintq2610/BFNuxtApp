<script setup lang="ts">
    const route = useRoute()
    const groupName = 'Group: ' + route.params.group
    const slugs = route.params.slugs
    console.log(route.params)
</script>


<template>
    <div>
        <p>{{ slugs }}</p>
        <p>{{ groupName }}</p>
        <p>{{ $route.params.group }} - {{ $route.params.id }}</p>
        <NuxtLink to="/">Home page</NuxtLink>
    </div>
</template>