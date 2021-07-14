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
          <nb-text>O símbolo da Aliança Rebelde é o pássaro estelar, que está presente nos uniformes e capacetes dos pilotos da Aliança. Apresentando semelhança com a fênix, esse símbolo representa o propósito da Aliança, que é acabar com o Império Galáctico.</nb-text>
        </nb-body>
      </nb-card-item> 
      <nb-card-item>
        <nb-body>
          <nb-text>A insígnia também foi adotada pela Resistência depois da Batalha de Endor, que marcou a vitória da Aliança sobre o Império.</nb-text>
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
import cardImage from "../../../../assets/simbolos/simb_alianca_rebelde.png";

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
