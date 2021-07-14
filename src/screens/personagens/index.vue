<template>
  <nb-container :style="{ backgroundColor: '#fff' }">
    <nb-header>
      <nb-left>
        <nb-button transparent :onPress="() => this.props.navigation.goBack()">
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>Personagens</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>
    <nb-content padder>
      <nb-list>
        <nb-list-item v-for="item in listItemArr" :key="item.text">
          <nb-left>
            <nb-thumbnail large :source="item.img" />
          </nb-left>
          <nb-body>
            <nb-text class="nome-pers">
              {{ item.text }}
            </nb-text>
            <nb-text
              :numberOfLines="14"
              :style="{ fontSize: 13, marginLeft: 0 }"
            >
              {{ item.note }}
            </nb-text>
          </nb-body>
          <nb-right>
            <nb-badge>
              <nb-text class="badge-team">{{ item.team }}</nb-text>
            </nb-badge>
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
import anakin from "../../../assets/personagens/anakin.png";
import chewbacca from "../../../assets/personagens/chewbacca.png";
import hansolo from "../../../assets/personagens/hansolo.png";
import leia from "../../../assets/personagens/leia.png";
import luke from "../../../assets/personagens/luke.png";
import obiwan from "../../../assets/personagens/obiwan.png";
import palpatine from "../../../assets/personagens/palpatine.png";
import ren from "../../../assets/personagens/ren.png";
import rey from "../../../assets/personagens/rey.png";
import yoda from "../../../assets/personagens/yoda.png";

export default {
  data() {
    return {
      listItemArr: [
        {
          img: anakin,
          text: "Anakin Skywalher/Darth Vader",
          note:
            "Darth Vader, nascido Anakin Skywalker, é um dos personagens centrais da saga, tendo sido um dos protagonistas, juntamente com Obi-Wan Kenobi, da trilogia prequel (mas se tornando o vilão secundário no terceiro filme após a morte do General Grievous), um dos antagonistas principais da trilogia original ao lado do Imperador Palpatine (porém acaba se redimindo no final), e um anti-herói póstumo na trilogia de sequência, sendo que suas ações ainda afetam o universo de Star Wars, sendo para o bem ou para o mal, principalmente quando se trata de seu neto, Ben Solo, o Kylo Ren, que tem por Vader uma admiração cega, e deseja mais do que tudo ser como ele (e até superá-lo). Vader participou de seis episódios (A Ameaça Fantasma, Ataque dos Clones, A Vingança dos Sith, Uma Nova Esperança, O Império Contra-Ataca e O Retorno de Jedi) [4][5] e também participou do spin-off Rogue One, além de ser constantemente citado em O Despertar da Força, Os Últimos Jedi e em A Ascenção Skywalker. Suas principais características são a armadura preta e a ruidosa respiração mecânica. É constantemente citado na cultura pop como um dos personagens mais icônicos de todos os tempos. É um dos poucos personagens da saga que estiveram presentes e tiveram ao menos uma menção em todos os 9 episódios lançados até hoje.",
          team: "I",
        },
        {
          img: ren,

          text: "Kylo Ren/Ben Solo",
          note:
            "Ben Solo, que mais tarde assumiu o nome de Kylo Ren, é o principal antagonista (ao lado de Palpatine) da terceira trilogia. Ele é filho da Princesa Leia com Han Solo e possui uma relação complicada com a protagonista Rey, a neta do Imperador, sendo ela sua principal rival, ao mesmo tempo em que eles progressivamente começam a se apaixonar um pelo outro. Foi treinado por Luke Skywalker, seu tio. Mas acabou indo para o Lado Sombrio da Força, tornando-se mestre dos Cavaleiros de Ren além de aliado e, após a morte de seu antecessor e mestre Snoke, Supremo Líder da Primeira Ordem, cerca de trinta anos após a Batalha de Endor.",
          team: "I",
        },
        {
          img: obiwan,
          text: "Obi-Wan Kenobi",
          note:
            "Obi-Wan Kenobi participou dos seis primeiros filmes (A Ameaça Fantasma, O Ataque dos Clones, A Vingança dos Sith, Uma Nova Esperança, O Império Contra-Ataca, e O Retorno do Jedi). Na trilogia original, foi interpretado por Sir Alec Guiness e nos outros três por Ewan McGregor, que interpretou a versão jovem do personagem. É um dos poucos personagens da série a aparecer nos seis primeiros episódios, dada a sua importância no enredo. Obi-Wan também teve uma referência na série da Disney Channel Boa Sorte, Charlie! quando seu nome foi dado para um dos personagens. O American Film Institute (AFI) em sua lista: '100 maiores heróis e vilões', elegeu Kenobi o 37º maior herói do cinema americano.",
          team: "F",
        },
        {
          img: luke,
          text: "Luke Skywalker",
          note:
            "Luke Skywalker é o protagonista da trilogia original, faz participação em Star Wars: O Despertar da Força em Star Wars: Os Últimos Jedi. É interpretado pelo ator norte-americano Mark Hamill. Um personagem essencial e importante na luta da Aliança Rebelde contra o Império Galáctico, é o irmão gêmeo da líder rebelde Princesa Leia Organa de Alderaan, foi amigo do mercenário Han Solo, aprendiz do Mestre Jedi yoda, e o filho do Jedi caído Darth Vader (Anakin Skywalker) e da Rainha de Naboo/Senadora da República Padmé Amidala. Ele é o tio e antigo mestre de Kylo Ren, antes deste ter se convertido ao Lado Negro da Força. Em 2008, o personagem foi escolhido pela revista Empire como o 54º maior personagem de filmes de todos os tempos.[1] Em sua lista dos 100 Maiores Personagens de Ficção, a Fandomania.com classificou Luke na 14ª posição",
          team: "F",
        },
        {
          img: leia,
          text: "Leia Organa",
          note:
            "Princesa Leia Organa ou General Leia Organa (seria nomeada como Leia Amidala Skywalker; porém foi batizada depois Leia Organa) é uma personagem fictícia interpretada por Carrie Fisher (1956-2016) nos filmes Star Wars: Episode IV - A New Hope, Star Wars: Episode V - The Empire Strikes Back, Star Wars: Episode VI - Return of the Jedi,[carece de fontes] Star Wars: Episode VII - The Force Awakens, Rogue One: A Star Wars Story e Star Wars: Episode VIII – The Last Jedi.",
          team: "F",
        },
        {
          img: yoda,
          text: "Mestre Yoda",
          note:
            "Yoda é um personagem fictício no universo Star Wars, criado por George Lucas. Ele aparece em seis filmes da saga, todos os filmes da trilogia prequela e da original exceto pelo episódio 4, e também aparece no episódio 8. Frank Oz, célebre criador dos Muppets, é o responsável pela sua voz. Possui apenas 76 centímetros, mas foi um sábio Mestre Jedi que liderou o Conselho Jedi por anos. Medindo 76 centímetros de altura, Yoda é um membro de uma espécie de nome desconhecido. Ele foi o Grão Mestre da Ordem Jedi durante as Guerras Clônicas, um dos membros mais importantes do Alto Conselho Jedi nos últimos dias da República Galáctica, e um dos mais sábios e poderosos Jedi de todos os tempos. Tendo vivido por muito tempo (veio a falecer com aprox. 900 anos de idade), ele tinha excepcionais habilidades no combate de sabre de luz, onde usava as técnicas acrobáticas da Forma IV, além de um fenomenal conhecimento sobre a Força. De 300 ABY até 19 ABY ele treinou quase todos os Jedi da Galáxia — como Grande Mestre, ele instruia todos os Younglings do Templo Jedi antes deles serem adotados por um mestre, tendo Anakin Skywalker sido uma exceção quanto a isso. O estudante mais importante de Yoda foi Luke Skywalker, o qual Yoda treinou para ser o futuro da Ordem após a sua quase completa destruição após a execução da Ordem 66. Tendo treinado o primeiro membro da Nova Ordem Jedi, Yoda serviu como canal entre as duas ordens, preservando a chama Jedi para uma próxima geração.",
          team: "F",
        },
        {
          img: hansolo,
          text: "Han Solo",
          note:
            "Han Solo é um personagem fictício, um dos protagonistas dos livros e filmes de ficção científica da série Star Wars (Uma Nova Esperança, O Império Contra-Ataca, O Retorno de Jedi, O Despertar da Força, Solo e A Ascensão Skywalker). No cinema, Han Solo foi interpretado pelo ator Harrison Ford. Para a série de filmes derivados, Han ganhou seu próprio spin-off, Solo: Uma História Star Wars, na qual o enredo gira ao redor das aventuras de sua juventude e é interpretada por Alden Ehrenreich. Han Solo é listado como um dos maiores e melhores personagens da história do cinema.",
          team: "F",
        },
        {
          img: palpatine,
          text: "Darth Sidious/Senador Palpatine",
          note:
            "Darth Sidious, nascido Sheev Palpatine, (também conhecido como Senador Palpatine, Supremo Chanceler Palpatine, Imperador Palpatine, ou simplesmente O Imperador) é o principal antagonista da franquia Star Wars (mais especificamente da Saga Skywalker), tendo sido o principal vilão na trilogia prequel, um dos dois principais, junto com Darth Vader, na trilogia original, e um dos dois principais, juntamente com Kylo Ren, na trilogia de sequência. Ele e Vader são os únicos vilões a ter um papel de relevância (dentro ou fora da tela) em todas as três trilogias. É interpretado pelo ator Ian McDiarmid. Assim como Yoda, Palpatine tem muitos detalhes de seu passado não revelados. Na carreira política, ele começou como um simples senador que representava apenas o sistema Naboo, seu sistema natal. E o segredo de seu sucesso foi: Paciência Infinita. Nunca sequer alterando seu tom de voz, Palpatine foi progredindo, progredindo até se tornar Supremo Chanceler da República, dando apenas um passo para se tornar Imperador. Já em sua carreira Sith, Sidious foi treinado nas artes Sith por Darth Plagueis, o Sábio, um munn capaz de influenciar os midi-chlorians a ponto de criar vida e enganar a morte. Sidious matou seu mestre enquanto ele dormia a a partir daí teve, ao contrário de muitos Sith, diversos aprendizes, que coincidentemente morriam em treinamento. Esses aprendizes são: Darth Maul, Conde Dooku e Darth Vader. Sidious também é avô de Rey (autoproclamada como Rey Skywalker), que, ironicamente, viria a se tornar a Última Jedi (em completa contradição com Sidious, que foi o Último Sith). Sidious também foi o responsável pela criação de Snoke, e por ajudar a atrair o herdeiro da família Skywalker (Ben Solo) ao Lado Sombrio.",
          team: "I",
        },
        {
          img: rey,
          text: "Rey",
          note:
            "Rey é uma personagem fictícia do universo Star Wars interpretada pela atriz Daisy Ridley. Ela é a principal protagonista da trilogia de sequência, aparecendo pela primeira vez em Star Wars: O Despertar da Força. Rey trabalhava a apanhar ferro-velho no planeta Jakku[5], onde foi abandonada com apenas 5 anos[6] e envolve-se no conflito entre a Resistência e a Primeira Ordem ao encontrar Finn, um stormtrooper desertor e BB-8, o droide do piloto da resistência Poe Dameron. Durante a sua jornada acaba desenvolvendo uma relação complexa com o (posteriormente) Líder Supremo da Primeira Ordem, Kylo Ren (filho de Han Solo com a Princesa Leia), a quem Rey nutre uma esperança de que possa voltar à luz (assim como Luke Skywalker tinha com Darth Vader). Ele é o seu principal adversário durante a nova saga, mesmo sendo também seu interesse amoroso. Rey descobre que o seu avô é o Imperador Palpatine, daí a mesma ser tão poderosa com a Força. O seu abandono foi uma forma dos seus pais a protegerem dele[7]. No final da sua jornada, ela confronta o seu avô (o último resquício dos Sith na galáxia) e derrota-o, evitando a volta dos Sith e mantendo assim o equilíbrio da Força estabelecido por Anakin Skywalker (Darth Vader) anos antes. Apesar de morrer após o confronto, é ressuscitada por Ben Solo. Subsquentemente adota o nome Rey Skywalker, cortando de vez os seus laços com o avô e com os Sith.",
          team: "F",
        },
        {
          img: chewbacca,
          text: "Chewbacca",
          note:
            "Chewbacca — apelido: Chewie — é o copiloto da nave Millennium Falcon e o melhor amigo de Han Solo, e um alienígena da raça Wookiee, oriundo do planeta Kashyyyk. Tendo participado de sete dos nove filmes da franquia (A Vingança dos Sith, Uma Nova Esperança, O Império Contra-Ataca, O Retorno do Jedi, O Despertar da Força, Os Últimos Jedi e A Ascensão Skywalker). Chewie é um excelente mecânico, muito sábio e temperamental. Foi interpretado por Peter Mayhew, que, com seus 2,15 m, foi escolhido por George Lucas. O Chewbacca é um republicano em A Vingança dos Sith, e um rebelde a partir de Uma Nova Esperança. Chewbacca nasceu em Kashyyyk 200 anos antes da Batalha de Yavin. Junto com outros wookiees ele combateu as forças de Palpatine (Darth Sidious) e do Império Galáctico, sendo o único sobrevivente de uma missão para salvar filhotes Wookiees de escravistas. Libertado por Han Solo, torna-se seu amigo, pois, segundo a cultura Wookiee, ele tem um débito de vida com aquele que o salvou. Chewbacca é casado com Mallatobuck e a tradição permite que ele se ausente do lar para cumprir sua dívida de honra. Ele e Han Solo se tornam contrabandistas a serviço dos Hutts. Chewie acompanha todas as aventuras e influencia o amigo a ajudar a Aliança Rebelde. Grande mecânico, esse wookie usa tal habilidade para resolver diversos problemas da nave Millennium Falcon, e em O Império Contra-Ataca, Chewbacca remonta C-3PO e quando ele é destruído pelos soldados imperiais na Cidade das Nuvens, em Bespin. Seu instinto animal também o colocou numa encrenca na lua florestal de Endor em O Retorno de Jedi, quando fareja uma presa (que na verdade era uma armadilha feita por Ewoks). Além de sua força natural e de suas garras retráteis, ele usa como arma principal sua besta a laser. Chewbacca é um jogador de xadrez dejarik holográfico muito temperamental, e seus adversários correm o risco de ter os braços arrancados durante a partida, se Chewie estiver perdendo.",
          team: "F",
        },
      ],
    };
  },
};
</script>

<style scoped>
.badge-team {
  font-weight: bold;
}
.nome-pers {
  margin-left: 0;
  margin-right: 0;
  color: darkblue;
  font-weight: bold;
}
</style>
