<template>
  <div>
    <h1>An error occured (error {{ error.statusCode }})</h1>
    <p><strong>{{ error.message }}</strong></p>
    <NuxtLink to="/"><strong>Go back to the Home page</strong></NuxtLink>
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'headless',
}
</script>