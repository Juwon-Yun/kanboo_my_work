<template>
   <h1>Filter</h1>
    <ul>
      <li> 
        <input type="checkbox" id="all" @click="selectedCheckbox">
        <label for="all">전체</label>
      </li>
      <li> 
        <input type="checkbox" id="common" @click="selectedCheckbox">
        <label for="common">공통</label>
      </li>
      <li> 
        <input type="checkbox" id="individual" @click="selectedCheckbox">
        <label for="individual">개인</label>
      </li>
      <li> 
        <input type="checkbox" id="notice" @click="selectedCheckbox">
        <label for="notice">공지</label>
      </li>
      <li> 
        <input type="checkbox" id="Emergency" @click="selectedCheckbox">
        <label for="Emergency">긴급</label>
      </li>
      <li> 
        <input type="checkbox" id="vacation" @click="selectedCheckbox">
        <label for="vacation">휴가</label>
      </li>
      <li> 
        <input type="checkbox" id="note" @click="selectedCheckbox">
        <label for="note">기타</label>
      </li>
    </ul>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  methods : {
    ...mapMutations({
      setFilterValue : 'scheduler/setFilterValue',
    }),
    selectedCheckbox(e){
      console.log(e.target.id)
      this.setFilterValue(e.target.id)
    },
  },
}
</script>

<style>

</style>