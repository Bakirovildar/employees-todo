<template>
  <div class="header-title">
    <span>Показаны записи 1-113 из 113.</span>
  </div>
  <div class="header">
    <div style="display: flex; align-items: center;">
      <input type="checkbox" class="inp-checkbox" @input="clickIsAllChecked" v-model="isChecked">
      <span class="header-fio">ФИО</span>
      <span class="header-d">Должность</span>
      <div class="header-sdd">
        <span class="header-status">Статус МО</span>
        <span class="header-date">Дата записи</span>
        <span class="header-date2">Дата прохождения</span>
      </div>
    </div>
    <div></div>
  </div>
</template>

<script>
export default {
  emits: ['clickAllChecked'],
  data() {
    return {
      isChecked: false
    }
  },
  methods: {
    clickIsAllChecked() {
      this.$emit('clickAllChecked', !this.isChecked)
    }
  }
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
  display: flex;
  justify-content: start;
  padding-right: 210px;
  color: black;
  width: 200px;
  min-width: 100px;
}

.header-d {
  padding-right: 145px;
  color: #E31243;
}

.header-sdd {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.header-status {
  color: #E31243;
  padding-right: 106px;
}

.header-date {
  color: #E31243;
}

.header-date2 {
  color: #E31243;
  padding-left: 92px;
}

.inp-checkbox {
  background: #E31243;
  margin-right: 16px;
}
</style>
