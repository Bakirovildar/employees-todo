<template>
  <div>
    <HeaderContent/>
    <EmployeesList :employees="employees"/>
  </div>
</template>

<script>
import HeaderContent from "@/components/HomePage/ContentEmployees/content/header/HeaderContent";
import EmployeesList from "@/components/HomePage/ContentEmployees/content/EmployeesList/EmployeesList";

export default {
  components: {EmployeesList, HeaderContent},
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
            name: 'Иванов Иван Иванович',
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
      }
    }
  }
}
</script>

<style scoped>

</style>
