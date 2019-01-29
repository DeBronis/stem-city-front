<template>
  <view class="container">
      <image-background :source="signup" class="signup">
      <image :source="logo" class="logo"></image>
      <view>
        <view class="input-container">
      <text-input class="input" auto-capitalize="none" v-model="zipCode" placeholder="Zip Code"/>
          <image :source="map" class="map"></image>
    <touchable-opacity  class="button2" :on-press="handleMap"
      :style="{padding: 10}">
       <text class="button-text">List View</text>
    </touchable-opacity>
    </view>
  </view>
  
</template>

<script>
import logo from "/Users/debroniswarren/playground2/stem-city-front/assets/images/imageedit_1_2155572343.png";

import signup from "/Users/debroniswarren/playground2/stem-city-front/assets/images/photo-1501769214405-5e5ee5125a02.jpeg";

import map from "/Users/debroniswarren/playground2/stem-city-front/assets/images/map.png";

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
      map: map,
      zipCode:"19144"
      
    };
  },
  methods:{
    handleMap() {
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
.map {
  width: 240%;
  height: 190%;
  position: relative; top: 47%; right: 35; 
  border-radius: 15;
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
  position: relative; left: 35%; top: -2%;
}
</style>