<template>
  <div class="main">
    <h3>List Of Engineers In ABC Software Company</h3>
    <table v-show="!isMobile">
      <thead>
        <td v-for="header in headers" :key="header.id">{{ header.text }}</td>
      </thead>

      <tbody>
        <tr v-for="item in items" :key="item.id">
          <td>{{ item.id }}</td>
          <td>{{ item.name }}</td>
          <td>{{ item.job_desc }}</td>
          <td>{{ item.email }}</td>
          <td>{{ item.prog_lang }}</td>
          <td>{{ item.salary }}</td>
        </tr>
      </tbody>
    </table>

    <table v-show="isMobile">
       <tr v-for="item in items" :key="item.id">
          <td>
            <span>Employee ID</span>
            <span>{{ item.id }}</span>
          </td>
          <td>
            <span>Employee Name</span>
            <span>{{ item.name }}</span>
          </td>
          <td>
            <span>Job Description</span>
            <span>{{ item.job_desc }}</span>
          </td>
          <td>
            <span>Email</span>
            <span>{{ item.email }}</span>
          </td>
          <td>
            <span>Programming Language</span>
            <span>{{ item.prog_lang }}</span>
          </td>
          <td>
            <span>Salary</span>
            <span>{{ item.salary }}</span>
          </td>
        </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    headers: [
      { text: "Employee ID", id: "1" },
      { text: "Employee Name", id: "2" },
      { text: "Job Description", id: "3" },
      { text: "Email", id: "4" },
      { text: "Programming Language", id: "5" },
      { text: "Salary", id: "6" }
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
      },
      {
        id: 6,
        name: "Andrey Phillips",
        job_desc: "Android Developer",
        email: "andreyphil@gmail.com",
        prog_lang: "Flutter",
        salary: "30000"
      },
      {
        id: 7,
        name: "Shirley Peace",
        job_desc: "Frontend Developer",
        email: "shirleypeace@gmail.com",
        prog_lang: "React",
        salary: "40000"
      },
      {
        id: 8,
        name: "Bisi Jonathan",
        job_desc: "Frontend Developer",
        email: "bisijo23@gmail.com",
        prog_lang: "Vue JS",
        salary: "35000"
      },
      {
        id: 9,
        name: "Tobais Onyekachi",
        job_desc: "Backend Engineer",
        email: "onyetoba@gmail.com",
        prog_lang: "Node JS",
        salary: "30000"
      },
      {
        id: 10,
        name: "Annabella Usman",
        job_desc: "Android Developer",
        email: "andreyphil@gmail.com",
        prog_lang: "Flutter",
        salary: "30000"
      }
    ],
    isMobile: false
  }),
  mounted() {
		this.collapseTable();
	},
  methods: {
		collapseTable() {
			if (window.innerWidth < 769) this.isMobile = true;
			else this.isMobile = false;
		}
	}
};
</script>

<style scoped>
.main {
  margin-top: 50px;
  letter-spacing: 0.0071428571em;
}
h3 {
  text-align: center;
  font-weight: bold;
  font-size: 1.2rem;
  line-height: 30px;
  color: #273052;
  margin-bottom: 0.8rem;
}
table {
  margin-left: auto;
  margin-right: auto;
  padding: 10px;
  border-radius: 6px;
  border: none;
  border-collapse: collapse;
  box-shadow: 0 2px 8px 2px rgba(39, 49, 82, 0.12);
}
thead {
  font-weight: bold;
  font-size: 1rem;
  color: #273052;
}
tr:nth-child(even) {
  background: rgba(190, 193, 203, 0.1) !important;
}
td {
  padding: 20px;
}

@media screen and (max-width: 768px) {
  table {
    width: 100%;
    padding: 1rem;
  }
  thead {
    display: none;
  }
  tr {
    display: grid !important;
    border-top: 1px solid#273052;
    border-bottom: 1px solid#273052;
  }
  td {
    display: flex;
    justify-content: space-between;
  }
}
</style>