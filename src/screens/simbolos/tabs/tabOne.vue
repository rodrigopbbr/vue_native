<template>
  <nb-container :style="{ backgroundColor: '#fff' }">
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
              >O símbolo da Ordem de Jedi, formado por asas e uma luz brilhante,
              representa a convicção dos Jedi em busca da paz.</nb-text
            >
          </nb-body>
        </nb-card-item>
        <nb-card-item>
          <nb-body>
            <nb-text
              >As asas e o sabre de luz (arma dos Jedi) representados no símbolo
              se referem às crenças e ao papel daqueles que pertencem à Ordem.
              Suas principais habilidades são a luta e a diplomacia.</nb-text
            >
          </nb-body>
        </nb-card-item>
        <nb-card-item>
          <nb-body>
            <nb-text
              >A Ordem Jedi é a guardiã da justiça e da paz, protetores da
              República Galáctica. Por sua capacidade de controlar as energias
              que regem o universo, conhecidas como Força, o grupo é responsável
              por proteger a galáxia do lado negro da força.</nb-text
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
  </nb-container>
</template>

<script>
import { Dimensions } from "react-native";
// import logo from "../../../assets/logo.png";
import cardImage from "../../../../assets/simbolos/simb_ordem_jedi.png";

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
.destaque {
  font-weight: bold;
  color:red;
}
</style>
