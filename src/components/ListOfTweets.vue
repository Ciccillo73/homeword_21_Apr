<template lang="html">
  <div >
    <h1>{{ tweet.name }}</h1>
    <p>{{ tweet.handle }}</p>
    <p>{{ tweet.img }}</p>
    <p>{{ tweet.tweet }}</p>
    <p>{{ tweet.likes }}</p>
  </div>
</template>

<script>
export default {
  name: 'list-of-tweets-item',
  props: ['tweet']

}
</script>

<style lang="css" scoped>
</style>
