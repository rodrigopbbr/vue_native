<template>
  <nb-content padder>
    <nb-card>
      <nb-card-item>
        <image
          :source="cardImage"
          class="card-item-image"
          :style="stylesObj.cardItemImage"
        />
        <nb-body>
          <nb-text
            >O símbolo da Resistência significa que a missão da Aliança Rebelde
            não tem fim. Semelhante ao símbolo da Aliança Rebelde, o único
            detalhe que os diferencia é a cor. O símbolo da Resistência é
            alaranjado.</nb-text
          >
        </nb-body>
      </nb-card-item>
    </nb-card>
    <nb-footer>
      <nb-footer-tab>
        <nb-button active full>
          <nb-text>Trilogias Star Wars</nb-text>
        </nb-button>
      </nb-footer-tab>
    </nb-footer>
  </nb-content>
</template>

<script>
import { Dimensions } from "react-native";
import cardImage from "../../../../assets/simbolos/simb_resistencia.png";

const deviceWidth = Dimensions.get("window").width;
export default {
  data() {
    return {
      // logo,
      cardImage,
      stylesObj: {
        cardItemImage: {
          resizeMode: "cover",
          flex: 1,
          width: deviceWidth / 1.18,
        },
      },
    };
  },
};
</script>

<style>
.card-item-image {
  align-self: center;
  height: 150;
}
</style>
