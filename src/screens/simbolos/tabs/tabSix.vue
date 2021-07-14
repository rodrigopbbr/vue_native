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
            >A Nova República nasce após a Batalha de Endor e estabelece de uma
            vez sua vitória sobre o Império. Por essa razão, seu símbolo, também
            uma adaptação da Aliança Rebelde representa a restauração da
            democracia.</nb-text
          >
        </nb-body>
      </nb-card-item>
      <nb-card-item>
        <nb-body>
          <nb-text
            >Além da mudança de cor, do vermelho para o azul, o símbolo da Nova
            República é envolto em raios amarelos.</nb-text
          >
        </nb-body>
      </nb-card-item>
      <nb-card-item>
        <nb-body>
          <nb-text
            >O símbolo era usado nos capacetes e uniformes dos pilotos da Nova
            República e também nas armaduras dos membros das Forças
            Especiais.</nb-text
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
import cardImage from "../../../../assets/simbolos/simb_nova_rep.png";

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
