<template>
  <app-navigation></app-navigation>
</template>

<script>
import { StackNavigator } from "vue-native-router";
import { DrawerNavigator } from "vue-native-router";
import MainScreen from "./Main";
import SignUpScreen from "./SignUp";

const Drawer = DrawerNavigator(
  {
    Main: MainScreen
  },
  {
    initialRouteName: "Main"
  }
);
const AppNavigation = StackNavigator(
  {
    Drawer: Drawer,
    Main: MainScreen,
    SignUp: SignUpScreen
  },
  {
    initialRouteName: "Main"
  }
);
export default {
  components: { AppNavigation }
};
</script>