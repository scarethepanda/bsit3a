<template>
  <v-card>
    <v-card-title>
      StudentData
      <v-spacer></v-spacer>
      <v-text-field v-model="search" append-icon="mdi-magnify" label="Search" single-line hide-details></v-text-field>
    </v-card-title>
    <v-data-table :headers="headers" :items="StudentData" :search="search">
      <template slot="item.actions" slot-scope="{item}">
        <v-btn color="#B80000"> DELETE</v-btn>
        <v-btn color="#0079FF"> EDIT</v-btn>
      </template>
    </v-data-table>

  </v-card>
</template>
<script>
export default {
  data() {
    return {
      search: '',
      headers: [
        {
          text: 'ID',
          align: 'start',
          sortable: false,
          value: 'StudentID',
        },
        { text: 'FirtsName', value: 'Firts_Name' },
        { text: 'LastName', value: 'Last_Name' },
        { text: 'MiddleName', value: 'Middle_Name' },
        { text: 'Course', value: 'Course' },
        { text: 'Year', value: 'Year' },
        { text: '', value: "actions" }
      ],
      StudentData: [

      {

Firts_Name: 'Franz Gerald',
StudentID: '21-00699',
Last_Name: 'Añasco',
Middle_Name: 'L.',
Course: 'BSIT',
Year: '3rd',
},

        {

          Firts_Name: 'Rolly',
          StudentID: '21-001',
          Last_Name: 'Arellano',
          Middle_Name: 'A.',
          Course: 'BSIT',
          Year: '3rd',
        },
        {

Firts_Name: 'Adrian',
StudentID: '21-002',
Last_Name: 'Icalina',
Middle_Name: 'B.',
Course: 'BSIT',
Year: '3rd',
},

{

Firts_Name: 'Andrew',
StudentID: '21-003',
Last_Name: 'Piñeda',
Middle_Name: 'C.',
Course: 'BSIT',
Year: '3rd',
},

{

Firts_Name: 'Billy',
StudentID: '21-004',
Last_Name: 'Castro',
Middle_Name: 'D.',
Course: 'BSIT',
Year: '3rd',
},


      ],
    }
  },
}
</script>