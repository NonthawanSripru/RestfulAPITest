<template>
<div name="home">
  <DataTable/>
</div>
</template>

<script>
  import DataTable from '../components/DataTable'

  export default {
    name: 'Home',

    components: {
      DataTable,
    },
  }
</script>
