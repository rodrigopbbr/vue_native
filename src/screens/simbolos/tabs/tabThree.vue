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
            >O símbolo do Império Galáctico é uma adaptação do símbolo utilizado
            pela República Galáctica, que antes com oito raios, agora passa a
            seis.</nb-text
          >
        </nb-body>
      </nb-card-item>
      <nb-card-item>
        <nb-body>
          <nb-text
            >Ele representa a mudança da democracia para o fascismo,
            transferência que é sublinhada pela cor do fundo, que de branco
            passa para negro. O símbolo era usado em bandeiras e uniformes, tudo
            para mostrar o poder do império.</nb-text
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
import cardImage from "../../../../assets/simbolos/simb_imperio_galactico.png";

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
