import user from '../assets/user.json';
<template>
  <div class="user-admin-dashboard">
    <Search v-model="searchTerm" />
    <Table :data="users" :searchTerm="searchTerm"/>    
  </div>
</template>

<script>
let setUserData = require('../assets/user.json')

import Table from './Table'
import Search from './Search'

export default {
  name: 'UserAdminDashboard',
  components: {
    Table,
    Search
  },
  data: () => ({
    users: setUserData,
    searchTerm: ''
  }),
}

// json from https://www.json-generator.com/
/*
[
  '{{repeat(10, 30)}}',
  {
    _id: '{{objectId()}}',
    index: '{{index()}}',
    picture: 'http://placehold.it/32x32',
    name: '{{firstName()}} {{surname()}}',
    email: '{{email()}}'
  }
]
*/
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
.user-admin-dashboard
  width auto  
</style>
