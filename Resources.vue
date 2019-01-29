<template>
  <view class="container">
      <image-background :source="signup" class="signup">
      <image :source="logo" class="logo"></image>
      <text class="title">Resources</text>
      <image :source="resources" class="resources"></image>
    </view>
    </template>

    <script>
import logo from "/Users/debroniswarren/playground2/stem-city-front/assets/images/imageedit_1_2155572343.png";

import signup from "/Users/debroniswarren/playground2/stem-city-front/assets/images/photo-1501769214405-5e5ee5125a02.jpeg";

import resources from "/Users/debroniswarren/playground2/stem-city-front/assets/images/resources(1).png";


export default {
  props: {
    navigation: {
      type: Object
    }
  },
  data() {
    return {
      signup: signup,
      logo: logo,
      resources: resources

    };
  },
  methods:{
    handleResources() {
      this.navigation.navigate("Resources"); 
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
  height: 50;
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
  height: 250;
  width: 150;
  display: flex;
  justify-content: space-evenly;
  position: relative; left: 15%; top: 14%;
  /* opacity: .50; */ 
}
.logo {
  width: 90%;
  height: 27%;
  position: relative; left: 5%; 
    
}
.resources {
  width: 75%;
  height: 65%;
  position: relative; top: -2%; left: 45;
  padding: 5; 
  
}
.signup {
  flex: 1;
  width: 100%;
}
.button2 {
  height: 55;
  width: 150;
  background-color: azure;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10;
  border-width: 2;
  align-content: center;
  opacity: .50;
  position: relative; left: 46%; bottom: -82%;
}
.title {
  font-family: Courier;
  font-size: 25;
  color:black;
  position: relative; left: 35%; top: -5%;
}
</style>
        
    