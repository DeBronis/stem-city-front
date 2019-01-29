<template>
  <app-navigation></app-navigation>
</template>

<script>
import { StackNavigator } from "vue-native-router";
import { DrawerNavigator } from "vue-native-router";
import MainScreen from "./Main";
import LogInScreen from "./LogIn";
import SignUpScreen from "./SignUp";
import MapScreen from "./Map";
import ResourcesScreen from "./Resources";
import { Font } from "expo";

const Drawer = DrawerNavigator(
  {
    Main: MainScreen,
    LogIn: LogInScreen
  },
  {
    initialRouteName: "Main"
  }
);
const AppNavigation = StackNavigator(
  {
    Drawer: Drawer,
    Main: MainScreen,
    SignUp: SignUpScreen,
    Map: MapScreen,
    Resources: ResourcesScreen
  },
  {
    initialRouteName: "Main"
  }
);
export default {
  components: { AppNavigation }
};
</script>

