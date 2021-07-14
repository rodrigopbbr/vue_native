<template>
  <root>
    <app-navigation></app-navigation>
  </root>
</template>

<script>
import {
  createAppContainer,
  createStackNavigator,
  createDrawerNavigator,
} from "vue-native-router";

import { Root } from "native-base";
import HomeScreen from "./screens/home/index.vue";
import TrilogiasScreen from "./screens/trilogias/index.vue";

import RegularActionSheetScreen from "./screens/actionSheet/regular";
import IconActionSheetScreen from "./screens/actionSheet/icon";

import CardShowcaseScreen from "./screens/card/cardShowcase";
import SideBarScreen from "./screens/sidebar/index.vue";

import TextAreaInputFormScreen from "./screens/form/textAreaInput";


const Drawer = createDrawerNavigator(
  {
    Home: { screen: HomeScreen },
    Trilogias: { screen: TrilogiasScreen },
  },
  {
    initialRouteName: "Home",
    contentOptions: {
      activeTintColor: "#e91e63",
    },
    contentComponent: SideBarScreen,
  }
);

const AppNavigation = createAppContainer(
  createStackNavigator(
    {
      Drawer: { screen: Drawer },
      RegularActionSheet: { screen: RegularActionSheetScreen },
      IconActionSheet: { screen: IconActionSheetScreen },
      NHCardShowcase: { screen: CardShowcaseScreen },
      TextArea: { screen: TextAreaInputFormScreen },
    },
    {
      initialRouteName: "Drawer",
      headerMode: "none",
    }
  )
);
export default {
  components: { Root, AppNavigation },
};
</script>
