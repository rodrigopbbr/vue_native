<template>
  <nb-container>
    <nb-header hasTabs>
      <nb-left>
        <nb-button transparent :onPress="() => this.props.navigation.goBack()">
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title> Curiosidades</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>

    <nb-tabs>
      <nb-tab heading="Tab1">
        <task-one />
      </nb-tab>
      <nb-tab heading="Tab2">
        <task-two />
      </nb-tab>
      <nb-tab heading="Tab3">
        <task-three />
      </nb-tab>
    </nb-tabs>
  </nb-container>
</template>

<script>
import TaskOne from "./tabs/taskOne";
import TaskTwo from "./tabs/taskTwo";
import TaskThree from "./tabs/taskThree";

export default {
  components: { TaskOne, TaskTwo, TaskThree }
};
</script>
