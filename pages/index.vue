<script setup lang="ts">
  import moment from "moment"
  
  const now = moment(new Date()).format('YYYY-MM-DD')

  const router = useRouter()
  console.log(router.options.routes)
</script>

<template>
  <div>
    <h1>Welcome to the homepage</h1>
    <app-alert>
      <div>TODAY: {{ now }}</div><br>
      <div>
        Routes:
        <div v-for="route in router.options.routes" :key="route.name">
          <a :href="route.path">{{ route.name }}</a>
        </div>
      </div>
    </app-alert>
  </div>
</template>