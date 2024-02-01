<template>
  <div>
    <!-- <button v-if="pageType=='reg'" @click="pageType='auth'"> Авторизация</button>
    <button v-else-if="pageType=='auth'" @click="pageType='reg'"> Регистрация</button>
    <p v-if="pageType=='reg'">welcome, do registration</p>
    <div v-else-if="pageType=='auth'">
      <input type="text">
    </div>
    <p v-else>u blocked</p>
    <input :type="inputType">
    <span :class="className"> Hello World </span>
    <button @click="className === 'first' ? (className = 'second') : (className = 'first')">Change color</button>
    <button @click="inputType === 'text' ? (inputType = 'number') : (inputType = 'text')">Change type</button> -->
    <!-- <p :style="{
      display: visibility ? 'block' : 'none'
    }">test</p> -->
    <!-- <p v-if="visibility">test</p>   -->
    <!-- <input type="text" v-model="styleText"> -->
    <!-- <button @click="styleText==='display:none' ? (styleText='display:block') : (styleText='display:none')" >Hide/show</button> -->
    <!-- <button @click="visibility = !visibility">Hide/show</button> -->
    <!-- <p :style="{
      color: color
    }">Hello world</p>
    <select name="" id="" v-model="color">
      <option v-for="(item, index) inarr" :key="item.value" :value="item.value">{{ index+1 + ' ' + item.title }}</option>
    </select> -->
    <div class="card">
      <h3>Tovar</h3>
      <h5>cost:200</h5>
      <div>
      <button v-if="styleText === 'display:none'" @click="styleText = 'display:block'">Buy</button>
      <div v-else :style="{ display: styleText }">
        <button @click="amount--">-</button>
        <span>Amount: {{ amount }}</span>
        <button @click="amount++">+</button>
      </div>
    </div>
    </div>
  </div>
</template>
//v-show
<script setup lang="ts">
import { ref } from 'vue';
const amount=ref<number>(0)
const color=ref('')
const arr= ref([
  {
    title: "Green",
    value: 'teal',

  },
  {
    title: "Red",
    value: 'red'
  },
  {
    title: "Blue",
    value:'blue'
  }
])


// const className = ref('first')
// const inputType = ref('text')

// const pageType = ref('auth')

const styleText=ref('display:none')
const visibility = ref(true)

</script>

<style scoped>
.first {
  color: red;
}

.second {
  color: teal;
}
</style>