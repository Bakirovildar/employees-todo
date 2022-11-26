<template>
  <div class="page-container">
    <div class="left-board">
      <LogoEmployees/>
    </div>

    <ContentEmployees :employees="employees" @deleteEmploy="deleteEmploy"/>
  </div>
</template>

<script>
import LogoEmployees from "@/assets/LogoEmployees";
import ContentEmployees from "@/components/HomePage/ContentEmployees/ContentEmployees";

export default {
  name: 'HomePage',
  components: {ContentEmployees, LogoEmployees},
  props: {
    msg: String
  },
  data() {
    return {
      employees: {
        title: 'Склад',
        list: [
          {
            id: 1,
            name: 'Иванов Иван Иванович',
            job: 'Водитель',
            status: 'Проходит',
            dateStart: '05.09.2022',
            dateGo: '05.09.2022'
          },
          {
            id: 2,
            name: 'Александров Андрей Сергеевич',
            job: 'Водитель',
            status: 'Проходит',
            dateStart: '05.09.2022',
            dateGo: '05.09.2022'
          },
          {
            id: 3,
            name: 'Иванов Иван Иванович',
            job: 'Водитель',
            status: 'Проходит',
            dateStart: '05.09.2022',
            dateGo: '05.09.2022'
          },
          {
            id: 4,
            name: 'Иванов Иван Иванович',
            job: 'Водитель',
            status: 'Проходит',
            dateStart: '05.09.2022',
            dateGo: '05.09.2022'
          },
          {
            id: 5,
            name: 'Иванов Иван Иванович',
            job: 'Водитель',
            status: 'Проходит',
            dateStart: '05.09.2022',
            dateGo: '05.09.2022'
          },
        ]
      },
    }
  },
  methods: {
    deleteEmploy(id) {
      const newFilteredList = this.employees.list.filter(employ => employ.id !== id)
      this.employees.list = newFilteredList
      if (id === 'Склад') {
        this.employees = {
          title: '',
          list: [
            {
              id: 0,
              name: '-',
              job: '-',
              status: '-',
              dateStart: '-',
              dateGo: '-'
            }]}
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.left-board {
  height: 100vh;
  width: 88px;
  padding-top: 48px;
  background: #FFFFFF;
  border-right: 1px solid #DBDADA;
  box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.1);
}

.page-container {
  display: flex;
}
</style>
