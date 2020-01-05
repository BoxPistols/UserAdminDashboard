<template>
  <div class="search">
    <input
      type="text"
      v-model="searchTerm"
      @input="$emit('input', $event.target.value)"
    />
  </div>
</template>

<script>
export default {
  name: 'Search',
  data: () => ({
    searchTerm: '',
  })
}
</script>

<style scoped lang="stylus">
  
</style>