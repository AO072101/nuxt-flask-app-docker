<template>
  <div>
    <h1 class="title">{{ data.message }}</h1>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData() {
    let data = await axios.get('/api')
    console.log(data)
    return data.data
  }
}
</script>

<style lang="scss">
.title {
  // color: $info;
  color: $primary;
}
</style>