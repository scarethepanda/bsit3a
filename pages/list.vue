<template>
  <v-data-table
    :headers="headers"
    :items="desserts"
    :items-per-page="5"
    class="elevation-1"
  ></v-data-table>
</template>

<script>
  export default {
    data () {
      return {
        headers: [
          {
            text: 'Student#',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'Lastname', value: 'lastname' },
          { text: 'Firstname', value: 'firstname' },
          { text: 'Middlename', value: 'middlename' },
          { text: 'Course', value: 'course' },
          { text: 'Section', value: 'section' },
        ],
        desserts: [
          
          
        ],
      }
    },
  }
  
</script>