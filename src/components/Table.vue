<template>
  <div class="table">
    <table>
      <thead>
        <tr>
          <th
            v-for="(title, index) in tableOrder"
            :key="index"
          >{{ title }}</th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="(user, index) in users"
          :key="index"
        >
          <td
            v-for="(key, idx) in tableOrder"
            :key="idx"
          >{{ user[key] }}</td>
        </tr>
      </tbody>
    </table>    
  </div>
</template>

<script>
  export default {
    name: 'Table',
    props: ['users'],
    data: () => ({
      tableOrder: ['name', 'picture', 'email']
    })
  }
</script>

<style scoped lang="stylus">
  
</style>