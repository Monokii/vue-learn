<template>
  <div class="black-bg" v-if="modal == true">
    <div class="white-bg">
      <h3>상세 페이지</h3>
      <p>내용</p>
      <button @click="modal = false">닫기</button>
    </div>
  </div>

  <nav class="navbar">
  <a v-for="m in memus" :key="m">{{ m }}</a>
  </nav>

  <h1>홈</h1>
  <div class="body">
    <div>
      <img :src="products[0].image" @click="modal = true">
      <div class="conbox">
        <div>
          <h2>{{ products[0].title }}</h2>
          <p>{{ products[0].price }}만원</p>  
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
          <button @click="modal = true">상세 보기</button>
          <button class="cr" @click="reportnum[0]++">신고</button><span>: {{ reportnum[0] }}</span>
        </div>        
      </div>

      <img :src="products[1].image" @click="modal = true">
      <div class="conbox">
        <div>
          <h2>{{ products[1].title }}</h2>
          <p>{{ products[1].price }}만원</p>  
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
          <button @click="modal = true">상세 보기</button>
          <button class="cr" @click="reportnum[1]++">신고</button><span>: {{ reportnum[1] }}</span>
        </div>        
      </div>

      <img :src="products[2].image" @click="modal = true">
      <div class="conbox">
        <div>
          <h2>{{ products[2].title }}</h2>
          <p>{{ products[2].price }}만원</p>  
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
          <button @click="modal = true">상세 보기</button>
          <button class="cr" @click="reportnum[2]++">신고</button><span>: {{ reportnum[2] }}</span>
        </div>        
      </div>

      <img :src="products[3].image" @click="modal = true">
      <div class="conbox">
        <div>
          <h2>{{ products[3].title }}</h2>
          <p>{{ products[3].price }}만원</p>  
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
          <button @click="modal = true">상세 보기</button>
          <button class="cr" @click="reportnum[3]++">신고</button><span>: {{ reportnum[3] }}</span>
        </div>        
      </div>

      <img :src="products[4].image" @click="modal = true">
      <div class="conbox">
        <div>
          <h2>{{ products[4].title }}</h2>
          <p>{{ products[4].price }}만원</p>  
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
          <button @click="modal = true">상세 보기</button>
          <button class="cr" @click="reportnum[4]++">신고</button><span>: {{ reportnum[4] }}</span>
        </div>        
      </div>

      <img :src="products[5].image" @click="modal = true">
      <div class="conbox">
        <div>
          <h2>{{ products[5].title }}</h2>
          <p>{{ products[5].price }}만원</p>  
        </div>
        <div style="display: flex; align-items: center; gap: 8px;">
          <button @click="modal = true">상세 보기</button>
          <button class="cr" @click="reportnum[5]++">신고</button><span>: {{ reportnum[5] }}</span>
        </div>        
      </div>

    </div>
  </div>
</template>

<script>
import condata from './assets/con-data.js';

export default {
  name: 'App',
  data(){
    return {
      modal : false,
      price : [40, 70, 100],
      products : condata,
      memus : ['홈', '상품', '소개'],
      reportnum : [0, 0, 0, 0, 0, 0],
    }
  },
  methods: {
    reportnn(){
      this.reportnum++;
    }
  },

  components: {
  }
}
</script>

<style>
.conbox {
  display: flex;
  flex-direction: column;
  margin-top: -20px;
}
.black-bg {
  width: 100%; height: 100%;
  justify-content: center;
  align-content: center;
  background-color: rgba(0, 0, 0, 0.4);
  position: fixed;
}
.white-bg {
  display: flex;
  max-width: 530px;
  flex-direction: column;
  background: rgb(36, 36, 36);
  border-radius: 10px;
  padding: 20px;
}
body {
  background-color: #000;
  justify-content: left;
  padding: 20px;
}
button {
  color: #000000;
  background-color: #ffffff;
  border-radius: 100px;
  border: none;
  padding: 12px 16px;
  transition: 0.2s;
}
button:hover {
  color: #000000;
  background-color: #e9efef;
  border: none;
  border-radius: 100px;
  padding: 12px 16px;
}
button:active {
  color: #000000;
  background-color: #d4dddd;
  border: none;
  border-radius: 100px;
  padding: 12px 16px;
}
.cr {
  color: #f45757;
  background-color: #000000;
  border: solid #992929;
  border-radius: 100px;
  padding: 12px 16px;
  transition: 0.2s;
}
.cr:hover {
  color: #f96a6a;
  background-color: #000;
  border: solid #f45757;
  border-radius: 100px;
  padding: 12px 16px;
}
.cr:active {
  color: #c62121;
  background-color: #000;
  border: solid #c62121;
  border-radius: 100px;
  padding: 12px 16px;
}
img {
  display: flex;
  width: fill;
  margin: 40px 0px 26px 0px;
  border-radius: 8px;
  border: 1px solid rgba(234, 237, 239, 0.3);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ffffff;
}
.navbar {
  display: flex;
  align-self: center;
  justify-content: center;
  padding: 5px 20px;
  background-color: #161717;
  border: solid #3b3c3e;
  border-radius: 100px;
}
.navbar a {
  padding: 14px 20px;
  border-radius: 16px;
  transition: 0.3s;
  align-self: center;
}
.navbar a:hover {
  padding: 14px 22px;
  background-color: #404448;
  border-radius: 26px;
}
.body {
  display: flex;
  flex-direction: column;
  margin-top: 60px;
}
</style>
