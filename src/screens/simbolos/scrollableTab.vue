<template>
  <nb-container>
    <nb-header hasTabs>
      <nb-left>
        <nb-button transparent :onPress="() => this.props.navigation.goBack()">
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title> Símbolos</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>

    <nb-tabs :renderTabBar="getScrollableTabComp">
      <nb-tab heading="Ordem Jedi">
        <tab-one />
      </nb-tab>
      <nb-tab heading="República Galáctica">
        <tab-two />
      </nb-tab>
      <nb-tab heading="Império Galáctico">
        <tab-three />
      </nb-tab>
      <nb-tab heading="Aliança Rebelde">
        <tab-four />
      </nb-tab>
      <nb-tab heading="Resistência">
        <tab-five />
      </nb-tab>
      <nb-tab heading="Nova República">
        <tab-six />
      </nb-tab>
      <nb-tab heading="Primeira Ordem">
        <tab-seven />
      </nb-tab>            
    </nb-tabs>
  </nb-container>
</template>

<script>
import React from "react";
import { ScrollableTab } from "native-base";
import TabOne from "./tabs/tabOne";
import TabTwo from "./tabs/tabTwo";
import TabThree from "./tabs/tabThree";
import TabFour from "./tabs/tabFour";
import TabFive from "./tabs/tabFive";
import TabSix from "./tabs/tabSix";
import TabSeven from "./tabs/tabSeven";

export default {
  components: { TabOne, TabTwo, TabThree, TabFour, TabFive, TabSix, TabSeven },
  methods: {
    getScrollableTabComp() {
      return <ScrollableTab />; 
    }
  }
};
</script>
