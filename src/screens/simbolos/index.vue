<template>
  <nb-container :style="{ backgroundColor: '#fff' }">
    <nb-header>
      <nb-left>
        <nb-button
          transparent
          :onPress="() => this.props.navigation.openDrawer()"
        >
          <nb-icon name="menu" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>Símbolos</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>
    <nb-content padder>
      <nb-list>
        <nb-list-item
          v-for="listItem in listItemArr"
          :key="listItem.route"
          button
          :onPress="() => this.props.navigation.navigate(listItem.route)"
        >
          <nb-left>
            <nb-text>
              {{ listItem.text }}
            </nb-text>
          </nb-left>
          <nb-right>
            <nb-icon name="arrow-forward" class="body-icon-color" />
          </nb-right>
        </nb-list-item>
      </nb-list>
    </nb-content>
    <nb-footer>
      <nb-footer-tab>
        <nb-button active full>
          <nb-text>Trilogias Star Wars</nb-text>
        </nb-button>
      </nb-footer-tab>
    </nb-footer>
  </nb-container>
</template>

<script>
export default {
  data() {
    return {
      listItemArr: [
        {
          route: "ScrollableTab",
          text: "Símbolos",
        },
        {
          route: "BasicTab",
          text: "Curiosidades (Tarefa)",
        },
      ],
    };
  },
};
</script>

<style>
.body-icon-color {
  color: #999;
}
</style>
