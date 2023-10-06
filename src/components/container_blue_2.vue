<template>
    <div class="box-container">
      <div class="box-1">
        <h3 v-html="header_one"></h3>
        <p v-html="box_one"></p>
      </div>
      <div class="box-2">
        <h3 v-html="header_two"></h3>
        <p v-html="box_two"></p>
      </div>
      <div class="box-3">
        <h3 v-html="header_three"></h3>
        <p v-html="box_three"></p>
      </div>
      <div class="box-4">
        <h3 v-html="header_four"></h3>
        <p v-html="box_four"></p>
      </div>
      <div class="box-5">
        <h3 v-html="header_five"></h3>
        <p v-html="box_five"></p>
      </div>
    </div>
  </template>
  

<script>
export default {
  name: 'container_blue_2',
  props: {
    header_one: String,
    header_two: String,
    header_three: String,
    header_four: String,
    header_five: String,

    box_one: String,
    box_two: String,
    box_three: String,
    box_four: String,
    box_five: String,
  },
};
</script>

<style>
.box-container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  background-color: #161F62;
  margin-top: 50px;
  padding: 20px;
}

.box-1,
.box-2,
.box-3,
.box-4,
.box-5 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-left: 50px;
  margin-right: 50px;
}

.box-1 h3,
.box-2 h3,
.box-3 h3,
.box-4 h3,
.box-5 h3 {
  font-family: 'Roboto', sans-serif;
  color: #fff;
  font-size: 24px;
  font-weight: 500;
  margin-bottom: 10px;
  margin-top: -40px;
}

.box-1 p,
.box-2 p,
.box-3 p,
.box-4 p,
.box-5 p {
  font-family: 'Roboto', sans-serif;
  color: #fff;
  font-size: 16px;
  font-weight: 400;
  text-align: center;
}
</style>
