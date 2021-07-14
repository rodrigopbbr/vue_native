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
            >A primeira ordem surge das cinzas do Império, formado por um grupo
            que buscava recuperar o seu domínio.</nb-text
          >
        </nb-body>
      </nb-card-item>
      <nb-card-item>
        <nb-body>
          <nb-text
            >Seu símbolo é um círculo com 16 raios dentro de uma moldura em
            forma de hexágono. Tanto as cores como os raios representados no
            círculo transmitem a ideia de perigo.</nb-text
          >
        </nb-body>
      </nb-card-item>
      <nb-card-item>
        <nb-body>
          <nb-text
            >A Ordem Jedi é a guardiã da justiça e da paz, protetores da
            República Galáctica. Por sua capacidade de controlar as energias que
            regem o universo, conhecidas como Força, o grupo é responsável por
            proteger a galáxia do lado negro da força.</nb-text
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
import cardImage from "../../../../assets/simbolos/simb_prim_ordem.png";

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
