<template>
  <div
      @click="clickItem"
      class="header-title">
    <div><span style="margin-right: 8px">{{ employees.title }}</span> <span
        style="font-weight: 500;font-size: 16px;line-height: 21px;color: #E31243;">{{ employees.list.length }}</span>
    </div>
    <div>
      <LogoEdit/>
      <LogoDelete/>
      <span v-if="!isOpen">
        <LogoClose/>
      </span>
      <span v-else>
        <LogoOpen/>
      </span>
    </div>
  </div>

  <div
      v-if="isOpen"
  >
    <div
        v-for="employ in employees.list"
        :key="employ.id">
      <div class="employ">
        <div class="employ-main">
          <input type="checkbox" class="inp-checkbox">
          <span class="header-fio">{{employ.name}}</span>
          <span class="header-d">{{employ.job}}</span>
          <div class="employ-sdd">
            <span class="header-status">{{employ.status}}</span>
            <span class="header-date">{{employ.dateStart}}</span>
            <span class="header-date">{{employ.dateGo}}</span>
          </div>
        </div>
        <div>
          <LogoSend/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LogoClose from "@/assets/LogoClose";
import LogoEdit from "@/assets/LogoEdit";
import LogoDelete from "@/assets/LogoDelete";
import LogoSend from "@/assets/LogoSend";
import LogoOpen from "@/assets/LogoOpen";

export default {
  components: {LogoOpen, LogoSend, LogoDelete, LogoEdit, LogoClose},
  props: ['employees'],
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    clickItem() {
      this.isOpen = !this.isOpen
    }
  }
}
</script>

<style scoped>

.header-title {
  display: flex;
  align-items: end;
  justify-content: space-between;
  margin-top: 30px;
  border-top: 1px solid #DBDADA;
  height: 70px;
  cursor: pointer;
}

.header-title:hover {
  background: ghostwhite;
}

.header-title:active {
  background: whitesmoke;
}

.employ {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-top: 1px solid #DBDADA;
  height: 70px;
  margin-right: 10px;
  cursor: pointer;
}

.employ-main {
  display: flex;
  align-items: center;
  padding-right: 20px;
}

.employ:hover {
  background: #F2F2F2;
}

.header-fio {
  color: black;
  width: 670px;
  text-align: start;
}

.header-d {
  padding-right: 160px;
  width: 70px;
  color: black;
}

.employ-sdd {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.header-status {
  color: #FF8800;
  width: 70px;
}

.header-date {
  color: black;
  width: 70px;
}

.inp-checkbox {
  background: #E31243;
  margin-right: 16px;
}
</style>
