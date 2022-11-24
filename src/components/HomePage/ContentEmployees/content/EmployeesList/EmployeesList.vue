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
        <div>
          <input type="checkbox" class="inp-checkbox">
          <span class="header-fio">{{employ.name}}</span>
          <span class="header-d">{{employ.job}}</span>
          <span class="header-status">{{employ.status}}</span>
          <span class="header-date">{{employ.dateStart}}</span>
          <span class="header-date">{{employ.dateGo}}</span>
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
  padding: 18px 18px;
  border-top: 1px solid #DBDADA;
  height: 53px;
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
  align-items: end;
  justify-content: space-between;
  padding: 0 18px 18px;
  border-top: 1px solid #DBDADA;
  height: 40px;
  margin-right: 10px;
  cursor: pointer;
}

.employ:hover {
  background: #F2F2F2;
}

.header-fio {
  padding-right: 227px;
  color: black;
}

.header-d {
  padding-right: 160px;
  color: black;
}

.header-status {
  padding-right: 100px;
  color: #FF8800;;
}

.header-date {
  padding-right: 100px;
  color: black;
}

.inp-checkbox {
  background: #E31243;
  margin-right: 16px;
}
</style>
