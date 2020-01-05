<template>
  <div class="table">
    <table>
      <thead>
        <tr>
          <th v-for="(val, index) in tableOrder" :key="index">{{ val }}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(row, index) in computedData" :key="index">
          <td v-for="(key, idx) in tableOrder" :key="idx">{{ row[key] }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
  export default {
    name: 'Table',
    props: ['data', 'searchTerm'],
    data: () => ({
      tableOrder: ['name', 'picture', 'email']
    }),
    computed: {
      computedData() {
        return this.data.filter(
          row =>
          row.name.includes(this.searchTerm) || row.email.includes(this.searchTerm))
      }
    }
  }
</script>

<style scoped lang="stylus">
table
  margin: auto
</style>