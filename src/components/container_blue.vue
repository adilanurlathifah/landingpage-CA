<template>
     <div class="box-container">
      <div class="box-1">
        <img :src="imgBoxOne">
        <p v-html="box_one"></p>
      </div>
      <div class="box-2">
        <img :src="imgBoxTwo">
        <p v-html="box_two"></p>
      </div>
      <div class="box-3">
        <img :src="imgBoxThree">
        <p v-html="box_three"></p>
      </div>
      <div class="box-4">
        <img :src="imgBoxFour">
        <p v-html="box_four"></p>
      </div>
    </div>
</template>

<script>
export default {
    name: 'container_blue',
    props: {
        imgBoxOne: String,
        imgBoxTwo: String,
        imgBoxThree: String,
        imgBoxFour: String,

        box_one: String,
        box_two: String,
        box_three: String,
        box_four: String,

    },
}
</script>

<style>
.box-container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly; 
  background-color: #161F62;
  margin-top: 50px;
  padding: 10px;
}

.box-container .box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-left: 50px; 
  margin-right: 50px; 
}

.box-container img {
  width: 70px;
  height: 70px;
  margin-bottom: 20px;
  margin-top: -30px;
}

.box-container p {
  color: #fff;
  font-size: 18px;
}

.box-container .box-1 {
  margin-left: 50px;
}
.box-container .box-2 {
  margin-left: 50px;
}
.box-container .box-3 {
  margin-left: 50px;
}
.box-container .box-4 {
  margin-left: 50px;
}
</style> 
