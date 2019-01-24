<template>
  <view class="container">
      <image class="background"
      :style="{width: 200, height: 100}"
      :source="{uri: 'https://i.ibb.co/LtgPmYz/Screen-Shot-2019-01-23-at-12-58-53-PM.png'}"
    ></image>
    <text class="title">Log In</text>
    <view class="input-container">
      <text-input class="input" auto-capitalize="none" v-model="firstName" placeholder="First Name"/>
      <text-input class="input" auto-capitalize="none"  v-model="lastName" placeholder="Last Name"/>
      <text-input class="input" auto-capitalize="none"  v-model="email" placeholder="Email"/>
    </view>
  </view>
</template>
<script>
export default {
  props: {
    navigation: {
      type: Object
    }
  },
  data() {
    return {
      message: "",
      myInput: "",
      firstName: "",
      lastName: "",
      email: "",
      
    };
  }
};
</script>
<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: flex-start;
  flex: 1;
}
.input {
  height: 50;
  width: 300;
  border-radius: 10;
  border-color: gray;
  border-width: 1;
  align-content: center;
  
}
.input-container {
    display: flex;
    align-content: center;
    justify-content: space-evenly;
    height: 600;
    width: 300;
}
</style>