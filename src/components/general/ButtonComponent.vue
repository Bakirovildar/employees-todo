<template>
  <div v-if="type === 1" class="button-red">
    <LogoAdd />
    <span>Добавить сотрудника</span>
  </div>
  <div v-if="type === 2" class="button-white">
    <LogoAddDep />
    <span>Создать новый отдел</span>
  </div>
  <div v-if="type === 3" class="button-blue">
    <span>Скачать список прошедших</span>
  </div>
  <div v-if="type === 3" class="button-blue">
    <span>Экспорт</span>
  </div>
  <div v-if="type === 3" class="button-blue1">
    <LogoUpload />
    <span>Загрузить списком</span>
  </div>
</template>

<script>
import LogoAdd from "@/assets/LogoAdd";
import LogoAddDep from "@/assets/LogoAddDep";
import LogoUpload from "@/assets/LogoUpload";
export default {
  components: {LogoUpload, LogoAddDep, LogoAdd},
  props: ['type']
}
</script>

<style scoped>
span {
  padding: 0 5px;
}

.button-red {
  background: #E31243;
  border-radius: 4px;
  padding: 0 9px;
  width: 200px;
  height: 40px;
  margin-right: 15px;
  color: white;
  display: flex;
  align-items: center;
  cursor: pointer;
}
.button-white {
  background: white;
  border-radius: 4px;
  padding: 0 9px;
  width: 200px;
  height: 40px;
  color: #E31243;
  border: 1px solid #E31243;
  display: flex;
  align-items: center;
  cursor: pointer;
}

.button-blue {
  height: 40px;
  padding: 0 5px;
  margin-right: 15px;
  background: #128BE3;
  border-radius: 4px;
  color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  cursor: pointer;
}

.button-blue1 {
  height: 40px;
  padding: 0 20px;
  margin-right: 15px;
  background: #128BE3;
  border-radius: 4px;
  color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  cursor: pointer;
}
</style>
