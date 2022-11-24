<template>
  <div class="header-title">
    <span>Показаны записи 1-113 из 113.</span>
  </div>
  <div class="header">
    <input type="checkbox" class="inp-checkbox">
    <span class="header-fio">ФИО</span>
    <span class="header-d">Должность</span>
    <span class="header-status">Статус МО</span>
    <span class="header-date">Дата записи</span>
    <span class="header-date">Дата прохождения</span>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.header-title {
  display: flex;
  justify-content: left;
  margin-top: 30px;
}

.header-title span {
  margin-left: 100px;
}

.header {
  padding: 0 18px;
  border-top: 1px solid #DBDADA;
  height: 53px;
  display: flex;
  align-items: end;
}

.header-fio {
  padding-right: 360px;
  color: #E31243;
}

.header-d {
  padding-right: 145px;
  color: #E31243;
}

.header-status {
  padding-right: 90px;
  color: #E31243;
}

.header-date {
  padding-right: 70px;
  color: #E31243;
}

.inp-checkbox {
  background: #E31243;
  margin-right: 16px;
}
</style>
