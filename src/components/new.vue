<template>
  <v-container>
    <v-data-table :headers="headers" :items="items" :items-per-page="5"></v-data-table>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    headers: [
      { text: "Employee ID", sortable: false, value: "id" },
      { text: "Employee Name", value: "name", sortable: false },
      { text: "Job Description", value: "job_desc", sortable: false },
      { text: "Email", value: "email", sortable: false },
      { text: "Programming Language", value: "prog_lang", sortable: false },
      { text: "Salary", value: "salary", sortable: false }
    ],
    items: [
      {
        id: 1,
        name: "Andrey Phillips",
        job_desc: "Android Developer",
        email: "andreyphil@gmail.com",
        prog_lang: "Flutter",
        salary: "30000"
      },
      {
        id: 2,
        name: "Shirley Peace",
        job_desc: "Frontend Developer",
        email: "shirleypeace@gmail.com",
        prog_lang: "React",
        salary: "40000"
      },
      {
        id: 3,
        name: "Bisi Jonathan",
        job_desc: "Frontend Developer",
        email: "bisijo23@gmail.com",
        prog_lang: "Vue JS",
        salary: "35000"
      },
      {
        id: 4,
        name: "Tobais Onyekachi",
        job_desc: "Backend Engineer",
        email: "onyetoba@gmail.com",
        prog_lang: "Node JS",
        salary: "30000"
      },
      {
        id: 5,
        name: "Annabella Usman",
        job_desc: "Android Developer",
        email: "andreyphil@gmail.com",
        prog_lang: "Flutter",
        salary: "30000"
      }
    ]
  })
};
</script>
