<script setup>
// import HelloWorld from './components/HelloWorld.vue';
</script>
<script>
export default {
  name: "App",
  data() {
    return {
      menus: ["Home", "Shop", "About"],
      products: [
        { name: "역삼동원룸", value: 50 },
        { name: "천호동원룸", value: 30 },
        { name: "마포구원룸", value: 20 },
      ],
      issueCount: [0, 0, 0],
    };
  },
  methods: {
    increase(i) {
      this.issueCount[i] += 1;
    },
  },
};
</script>

<template>
  <div class="black-bg dialog">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지내용임</p>
    </div>
  </div>

  <div class="menu">
    <a href="" v-for="(menu, i) in menus" :key="i">{{ menu }}</a>
  </div>
  <div>
    <img src="./assets/room0.jpg" alt="" class="room-img" />
    <h4>{{ products[0].name }}</h4>
    <p>{{ products[0].value }}</p>
    <!-- <button @click="issueCount++">허위매물신고</button> -->
    <button @click="increase(0)">허위매물신고</button>
    <!-- <button @mouseover="issueCount += 1">허위매물신고</button> -->
    <span>신고수: {{ issueCount[0] }}</span>
  </div>
  <div>
    <img src="./assets/room1.jpg" alt="" class="room-img" />
    <h4>{{ products[1].name }}</h4>
    <p>{{ products[1].value }}</p>
    <button @click="increase(1)">허위매물신고</button>
    <span>신고수: {{ issueCount[1] }}</span>
  </div>
  <div>
    <img src="./assets/room2.jpg" alt="" class="room-img" />
    <h4>{{ products[2].name }}</h4>
    <p>{{ products[2].value }}</p>
    <button @click="increase(2)">허위매물신고</button>
    <span>신고수: {{ issueCount[2] }}</span>
  </div>
</template>
<style>
div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 2rem;
}
.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 2rem;
}
.room-img {
  width: 100%;
  margin-top: 40px;
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
