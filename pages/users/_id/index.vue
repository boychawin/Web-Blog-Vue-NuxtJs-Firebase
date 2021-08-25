<template>
    <h1>Posts page id: {{$route.params.id}}</h1>
</template>

<script>
export default {
  validate({ params }) {
    // Must be a number
    return /^\d+$/.test(params.id)
  }
}
</script>