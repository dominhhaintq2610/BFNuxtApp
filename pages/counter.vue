<script setup>
  useHead({
    titleTemplate: (titleChunk) => {
      return titleChunk ? `${titleChunk} - counter` : 'Counter';
    }
  })

  const counter = useCounter()
</script>

<template>
  <div>
    <div>
        Counter: {{ counter }}
        <button @click="counter++">
        +
        </button>
        <button @click="counter--">
        -
        </button>
    </div>
    <NuxtLink to="/">Home page</NuxtLink>
  </div>
</template>