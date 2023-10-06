<template>
  <div class="custom_button">
    <button
      :class="{ 'custom-button-blue': buttonType === 'blue', 'custom-button-white': buttonType === 'white' }"
      @click="handleClick"
    >
      {{ label }}
    </button>
  </div>
</template>

<script>
export default {
  props: {
    label: String,
    buttonType: String,  
  },
  methods: {
    handleClick() {
      this.$emit('click');
    },
  },
};
</script>

<style>
.custom_button .custom-button-blue {
  background-color: #004ECB;
  color: white;
  border: 0.75px solid #004ECB;
  border-radius: 5px;
  padding: 10px 40px;
  cursor: pointer;
  font-size: 17px;
  box-shadow: 0 0 15px rgba(0,0,0,.15);
}

.custom_button .custom-button-blue:hover {
  background: #2070f2;
  color: white;
}

.custom_button .custom-button-white {
  background-color: #ffffff;
  color: #004ECB;
  border: 0.75px solid #004ECB;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
  border-color: #004ECB;
  font-size: 15px;
}

.custom_button .custom-button-white:hover {
  background: #004ECB;
  color: white;
}
</style>