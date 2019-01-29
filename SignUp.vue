<template>
  <view class="container">
      <image-background :source="signup" class="signup">
      <image :source="logo" class="logo"></image>
    <text class="title">Sign Up</text>
    <view class="input-container">
      <text-input class="input" auto-capitalize="none" v-model="firstName" placeholder="First Name"/>
      <text-input class="input" auto-capitalize="none"  v-model="lastName" placeholder="Last Name"/>
      <text-input class="input" auto-capitalize="none"  v-model="email" placeholder="Email"/>
      <text-input class="input" auto-capitalize="none"  v-model="password" placeholder="Password"/>
    </view>
    <view>
    <touchable-opacity  class="button2" :on-press="handleSignUp"
      :style="{padding: 10}">
       <text class="button-text">Submit</text>
    </touchable-opacity>
    </view>
  </view>
</template>
<script>
import logo from "/Users/debroniswarren/playground2/stem-city-front/assets/images/imageedit_1_2155572343.png";

import signup from "/Users/debroniswarren/playground2/stem-city-front/assets/images/photo-1501769214405-5e5ee5125a02.jpeg";
export default {
  props: {
    navigation: {
      type: Object
    }
  },
  data() {
    return {
      myInput: "",
      firstName: "",
      lastName: "",
      email: "",
      password: "",
      signup: signup,
      logo: logo
    };
  },
  methods:{
    handleSignUp() {
      this.navigation.navigate("Map"); 
    }
  }
};
</script>

<style>
.container {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
}
.input {
  height: 60;
  width: 300;
  border-radius: 10;
  border-color: black;
  border-width: 1;
  align-content: center;
  font-family: Courier;
  font-size: 25;
  color:black;
  
}
.input-container {
  height: 315;
  width: 150;
  display: flex;
  justify-content: space-evenly;
  position: relative; left: 15%; bottom: -3%;
  /* opacity: .50; */ 
}
.logo {
  width: 90%;
  height: 27%;
  position: relative; left: 5%; 
    
}
.signup {
  flex: 1;
  width: 100%;
}
.button2 {
   height: 75;
  width: 150;
  background-color: azure;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10;
  border-width: 2;
  align-content: center;
  opacity: .50;
  position: relative; left: 30%; bottom: -110%;
}
.button-text{
  font-family: Courier;
  font-size: 25;
  color:black;
}
.title {
  font-family: Courier;
  font-size: 30;
  color:black;
  position: relative; left: 35%; top: -4%;

}
</style>

