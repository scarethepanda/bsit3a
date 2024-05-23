<template>
  <v-card>
  <v-data-table
    :headers="headers"
    :items="studentData"
    :items-per-page="5"
    class="elevation-1"
  >
  <template slot="item.action" slot-scope="">
<v-btn dark color="#43A047"> <v-icon left>mdi-eye</v-icon>VIEW</v-btn>
<v-btn dark color="#01579B"> <v-icon left>mdi-pencil</v-icon>EDIT</v-btn>
<v-btn dark color="#D32F2F"> <v-icon left>mdi-trash-can</v-icon>DELETE</v-btn>
  </template>
  
  </v-data-table>
</v-card>
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
            value: 'attributes.student_no',
          },
          { text: 'Lastname', value: 'attributes.last_name' },
          { text: 'Firstname', value: 'attributes.first_name' },
          { text: 'Middlename', value: 'attributes.middle_name' },
          { text: 'Course', value: 'attributes.course' },
          { text: 'Section', value: 'attributes.section' },
        ],
        studentData: [
          
          
        ],
      }
    },

methods: {
getStudentList(){
  this.$axios.get("http://localhost:1337/api/student-lists")
  .then(response => {
    console.log("Success");
    console.log(response.data.data);
    this.studentData = response.data.data;
  })
  .catch(error => {
    console.log("error")
  })
}
},

mounted(){
console.log("Auto run")
this.getStudentList()
}

  };
  
</script>