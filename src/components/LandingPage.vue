<template>
  <v-app>

      <v-card variant="flat" class="principalCard">
        <div class="spacingCol d-flex flex-column flex-md-row flex-lg-row justify-space-between">
          <div class="divText pa-5 mt-12"> 
            <p class="titlename"><v-icon>mdi-flash</v-icon>PLATAFORMA EXCLUSIVA</p>
            <h1 class="mt-4 mb-5">Conecte-se com outros servidores públicos e amplie seu conhecimento</h1>
            <p class="mr-3">
              Com o Explica Aqui, você tira suas dúvidas, aprende com os melhores especialistas e constrói uma rede de contatos para se manter atualizado e avançar na carreira.
            </p>
            <div class="d-flex flex-column flex-md-row justify-space-between">
              <v-text-field
                class="insertButton"
                bg-color="#FFFFFF"
                variant="flat"
                density="compact"
                rounded="xl"
                placeholder="Insira seu e-mail"
              >
              </v-text-field> 
              <v-btn 
                rounded="xl" 
                class="registerButton"
              >CADASTRE-SE AGORA
              </v-btn>
            </div>
          </div>
          <div class="pa-5"> 
            <div class="imagemPrincipal mx-auto"> 
              <v-img
                aspect-ratio="16/9"
                cover
                src="/src/assets/tablet-digital-pode-resolver-o-problema 1.png"
              ></v-img>
              <v-img
                class="spacingImage1"
                src="/src/assets/image-PhotoRoom.png-PhotoRoom.png"
              >
              </v-img>
              <v-img
                src="/src/assets/tiresuaduvida.png"
                class="spacingImage2"
              >
              </v-img>
            </div>
          </div>
        </div>
      </v-card>
      <div class="principalDiv d-flex flex-column flex-md-row flex-lg-row">
        <div>
          <img src="/src/assets/image-removebg.png" class="dimensionImg" />
        </div>
        <div class="mx-auto justify-center colCards">
          <v-row>
            <h1 class="titleDiv2">
              Aprenda, colabore com colegas e se desenvolva profissionalmente
            </h1>
            <v-col
              v-for="(variant, i) in variants"
              :key="i"
              cols="12"
              md="12"
              lg="6"
              xl="5"
            >
              <v-card class="secondCard" variant="flat">
                <v-card-item>
                  <div class="spacingContent">
                    <v-sheet class="cardIcons" variant="tonal" :color="colors[i]">
                      <v-icon :color="colorIcon[i]" size="17" class="colorIcon">
                        {{ variant.icon }}
                      </v-icon>
                    </v-sheet>
                    <h6 class="classTitle">{{ variant.title }}</h6>
                    <div>{{ variant.description }}</div>
                    <v-divider
                      class="mt-7 d-md-none d-xl-none d-lg-none"
                      :thickness="2"
                    ></v-divider>
                  </div>
                </v-card-item>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </div>
      <div class="d-flex justify-center">
      <v-card class="blueCard">
        <div class="d-flex justify-center flex-column flex-md-row">
          <div class="spacingCol1">
            <p class="fontSubtitle">
              <v-icon class="mr-2">mdi-cellphone-link</v-icon>DISPONÍVEL EM
              TODAS AS PLATAFORMAS
            </p>
            <h1>
              Junte-se à maior comunidade de servidores públicos do Brasil.
            </h1>
          </div>
          <div class="justify-center mx-auto spacingCol2">
            <v-text-field
              class="emailInput"
              bg-color="#F6F5FF"
              variant="flat"
              density="compact"
              rounded="xl"
              placeholder="Digite seu e-mail"
            >
            </v-text-field>
            <v-btn rounded="xl" class="btnRegister">CADASTRE-SE AGORA </v-btn>
          </div>
        </div>
      </v-card>
    </div>

    <div class="mt-10">
      <div>
        <v-col cols="12">
          <h1 class="marginTitle1">
            Comece sua jornada no Explica Aqui agora mesmo!
          </h1>
        </v-col>
        <div class="flex-column flex-md-row">
          <div
            v-for="(itens, x) in itens2"
            :key="x"
            class="d-flex justify-center mx-auto"
          >
            <v-card class="spacingCardsIcons" variant="flat">
              <v-card-item>
                <div>
                  <v-sheet
                    variant="tonal"
                    :color="colors2[x]"
                    :height="40"
                    :width="40"
                    rounded="lg"
                  >
                    <v-icon :color="colorIcon2[x]" size="17" class="colorIcon"
                      >{{ itens.icon2 }}
                    </v-icon>
                  </v-sheet>
                  <h6 class="classTitle">{{ itens.title2 }}</h6>
                  <div>{{ itens.description }}</div>
                  <div class="mt-4">{{ itens.description2 }}</div>
                </div>
              </v-card-item>
              <v-divider
                class="mt-4 mb-4 d-md-none d-xl-none d-lg-none"
                :thickness="2"
              ></v-divider>
            </v-card>
          </div>
        </div>
      </div>
    </div>

    <div class="d-flex justify-center">
      <v-card variant="flat" class="purpleCard justify-center text-center">
        <v-col class="marginTitle">
          <h1>
            Escolha o plano que melhor atende às suas necessidades
          </h1>
        </v-col>
        <div class="d-flex justify-center flex-column flex-md-row mt-10">
          <v-card 
            variant="flat" 
            class="subCard1 mx-auto"
          >
            <h1 class="mt-8 mb-3">Gratuito</h1>
            <p>A escolha perfeita para quem busca uma introdução à nossa comunidade.</p>
            <v-row class="mt-5 mb-5 pl-4">
              <p class="pt-6">R$</p>
              <h1 class="priceFont">0</h1>
            </v-row>
            <v-divider></v-divider>
            <div v-for="(list, z) in miniumList" :key="z">
              <p class="mt-5 mb-5">
                <v-icon size="24" class="pr-3">{{ list.icon }}</v-icon>
                {{ list.text }}
              </p>
            </div>
            <v-divider></v-divider>
            <v-text-field
              class="emailInput2"
              variant="outlined"
              density="compact"
              rounded="xl"
              placeholder="Insira seu e-mail"
            >
            </v-text-field>
            <v-btn 
              rounded="xl" 
              class="btnRegister2"
              variant="outlined"
            >CADASTRE-SE AGORA</v-btn>
          </v-card>

          <v-card align="start" variant="flat" class="subCard2 mx-auto">
            <h1 class="mt-8 mb-4">
              <v-icon>mdi-asterisk</v-icon>
              Premium
            </h1>
            <p>Uma experiência que vai além das expectativas. Sua ascensão profissional começa aqui.</p>
            <v-row class="mt-5 mb-5 pl-4">
              <p class="pt-6">R$</p>
              <h1 class="priceFont">19,90</h1>
              <p class="pt-6 pl-2">/ MÊS</p>
            </v-row>
            <v-divider></v-divider>
            <div v-for="(list2, y) in miniumList2" :key="y">
              <p class="mt-5 mb-5"><v-icon size="24" class="pr-3">{{ list2.icon }}</v-icon>{{ list2.text }}</p>
            </div>
            <v-divider></v-divider>
            <v-text-field
              class="emailInput3"
              variant="outlined"
              density="compact"
              rounded="xl"
              placeholder="Insira seu e-mail"
            >
            </v-text-field>
            <v-btn 
              rounded="xl" 
              class="btnRegister"
            >CADASTRE-SE AGORA</v-btn>
          </v-card>
        </div>
      </v-card>
    </div>

    <div class="d-flex flex-column flex-md-row justify-center mt-12 mx-auto">
      <div class="mr-8">
        <p class="styleFaq"><v-icon class="pr-2">mdi-forum-plus</v-icon>FAQ</p>
        <h1>Perguntas Frequentes</h1>
      </div>
      <div class="spacingCols">
        <v-list v-model:opened="open">
          <v-list-group v-for="(item, i) in items" :key="i" :value="item.title">
            <template v-slot:activator="{ props }">
              <v-list-item v-bind="props" class="bold-title">{{ item.title }}
              </v-list-item>
              <v-divider :thickness="2"></v-divider>
            </template>
            <v-list-item
              v-for="title in item.expandedText.split('\n')"
              :key="title"
              class="ml-n4"
              >
              {{ title }}
            </v-list-item>
          </v-list-group>
        </v-list>
      </div>
    </div>

    <div class="d-flex justify-center">
      <v-card class="blueCard2">
        <div class="d-flex justify-center">
          <div class="spacingCol3">
            <p class="fontSubtitle"><v-icon class="mr-2">mdi-wifi</v-icon>ACESSO ILIMITADO</p>
            <h1>Dê o primeiro passo em direção ao seu desenvolvimento profissional.</h1>
          </div>
          <div class="justify-center spacingCol2">
            <v-text-field
              class="emailInput"
              bg-color="#F6F5FF"
              variant="flat"
              density="compact"
              rounded="xl"
              placeholder="Digite seu e-mail"
            >
            </v-text-field>
            <v-btn 
              rounded="xl" 
              class="btnRegister"
            >CADASTRE-SE AGORA
            </v-btn>
          </div>
        </div>
      </v-card>
    </div>      
  </v-app>
</template>


<script>
import { VApp } from 'vuetify/lib/components/index.mjs';

export default {
  data() {
    return {
      colors: ['#F6F5FF','#FFF6FA','#FEF9D5CC', '#F3F3F5'],
      colorIcon: ['#4E42FF','#FF57A7','#FFDE13', '#1C1B1F'],
      variants: [
        { icon: 'mdi-message-text-outline', title: 'Respostas com quem entende', description: 'Obtenha respostas precisas e atualizadas de profissionais qualificados da área.' },
        { icon: 'mdi-chart-box-plus-outline', title: 'Aprimore suas habilidades', description: 'Transforme cada interação em uma oportunidade única de desenvolvimento profissional' },
        { icon: 'mdi-web', title: 'Cresça em comunidade', description: 'Compartilhe experiências, insights e desenvolva relacionamentos profissionais.' },
        { icon: 'mdi-gesture-tap-hold', title: 'Conhecimento na palma da mão', description: 'Garanta uma experiência de aprendizado contínuo onde quer que você esteja.' }
      ],
      colors2: ['#F6F5FF','#FFF6FA','#FEF9D5CC'],
      colorIcon2: ['#4E42FF','#FF57A7','#FFDE13'],
      itens2: [
        { icon2: 'mdi-message-text-outline', title2: 'Complete seu cadastro', description: 'Para começar a usar o Explica Aqui, insira seu e-mail e clique em “Cadastre-se agora”. ', description2: 'Em seguida, preencha o formulário com suas informações pessoais.'},
        { icon2: 'mdi-chart-box-plus-outline', title2: 'Confirme seus dados', description: 'Para garantir a segurança da sua conta, confirme o código de verificação enviado para o número de telefone fornecido.', description2: 'Sua segurança é nossa prioridade.'},
        { icon2: 'mdi-web', title2: 'Acesse a plataforma', description: 'Você está pronto para explorar a plataforma! Faça ou responda perguntas e conecte-se com seus colegas.', description2: 'Bem-vindo ao Explica Aqui!'},
      ],
      miniumList: [
        { icon: 'mdi-check-decagram', text: 'Acesso à comunidade e recursos básicos' },
        { icon: 'mdi-check-decagram', text: 'Envio de até 5 perguntas mensais' },
        { icon: 'mdi-close-circle-outline', text: 'Respostas verificadas por especialistas' },
      ],
      miniumList2: [
        { icon: 'mdi-check-decagram', text: 'Todos os benefícios do plano gratuito' },
        { icon: 'mdi-check-decagram', text: 'Sem limite de perguntas ou respostas' },
        { icon: 'mdi-check-decagram', text: 'Respostas verificadas por especialistas' },
      ],
      items: [
      { title: 'O que é o Explica Aqui?', expandedText: 'A comunidade ExplicaAqui é formada por servidores públicos que compartilham o interesse comum em fomentar o conhecimento técnico, promover o aprendizado e facilitar a troca de informações em diversas especializações. Pode-se ainda dizer que o ExplicaAQui é uma comunidade engajada na promoção de um ambiente colaborativo entre servidores públicos, com a missão final de contribuir para a prestação de serviços públicos de alto padrão à sociedade.' },
        { title: 'Quais são os benefícios do Explica Aqui?', expandedText: 'Acesso a diversidade de experiências, aprendizado Contínuo, resolução de Problemas, feedback construtivo, mentoria Informal, atualização de tendências, acesso a recursos exclusivos, colaboração e projetos conjuntos' },
        { title: 'Como posso me cadastrar no Explica Aqui?', expandedText: 'Acesse a página inicial do ExplicaAqui e escolha “cadastrar”, preencha seus dados corretamente e comece a participar da maior comunidade de servidores públicos do Brasil.' },        
        { title: 'Quais são os planos disponíveis no Explica Aqui?', expandedText: 'São dois os planos disponíveis: Gratuíto e Premium. A diferença entre eles é que no plano Premium o membro tem acesso a recursos exclusivos, tais como: respostas verificadas, webinars, cursos, e-books e ferramentas especiais.' },
        { title: 'Qual a diferença entre respostas verificadas e não verificadas?', expandedText: 'As respostas não verificadas são fornecidas por membros que informaram livremente conhecimento específico para a área em questão. Já as respostas verificadas são fornecidas por especialistas e ferramentas identificados e verificados pela equipe do ExplicaAqui.' },
        { title: 'Posso trocar do Plano Gratuito para o Premium a qualquer momento?', expandedText: 'Sim, é possivel a qualquer momento efetuar a toca de plano.' },
      ],
      open: [],
    };
  },
};
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Sora&display=swap');

* {
font-family: 'Sora', sans-serif;
}

.principalCard {
  background-color: #edecff;
  height: 552px;
  max-width: 100%;
}

@media screen and (max-width: 600px) {
  .principalCard {
    height: 1000px;
  }
}

@media screen and (max-width: 960px) {
  .principalCard {
    max-width: 150%;
    max-width: 150%;
    height: 1000px;
  }
  .spacingCol {
    margin-left: 5%;
    margin-right: 5%;
  }
}

@media screen and (min-width: 959px) and (max-width: 1720px) {
  .principalCard {
    max-width: 150%;
    max-width: 150%;
    height: 500px;
  }
}

@media screen and (min-width: 960px) and (max-width: 1280px) {
  .spacingCol {
    margin-left: 8%;
    margin-right: 8%;
  }
}

@media screen and (min-width: 1280px) and (max-width: 1920px) {
  .spacingCol {
    margin-left: 10%;
    margin-right: 10%;
  }
  .spacingContent {
    width: 260px;
    height: 208px;
  }
} 

.titlename {
  font-weight: 600;
  font-size: 14px;
}

.insertButton {
  height: 40px;
  margin-top: 15px;
  font-weight: 600 !important;
  margin-right: 7px;
}

.registerButton {
  background-color: #161B33 !important;
  color: white !important;
  height: 40px;
  margin-top: 15px;
  margin-right: 7px;
  font-weight: 600 !important;
  font-size: 13px;
}

@media screen and (min-width: 1600px) and (max-width: 1920px) {
  .divText {
    margin-left: 8%;
    margin-right: 8%;
  }
}

.principalDiv {
  margin-left: 10%;
  margin-right: 10%;
}

@media screen and (max-width: 600px) {
  .principalDiv {
    margin-left: 10px ;
    margin-right: 10px;
  }
}

.dimensionImg {
  width: 470px;
  height: 600px;
}

.titleDiv2 {
  margin-top: 40px;
  margin-left: 15px;
}

@media screen and (max-width: 600px) {
  .colCards {
    margin-left: 0px ;
    margin-right: 0px;
  }
  .titleDiv2 {
    margin-left: 30px ;
    margin-right: 30px;
  }
}

@media screen and (min-width: 960px) and (max-width: 1200px) {
  .colCards {
    margin-top: 50px ;
  }
}
/* específico ^^^ */

@media screen and (min-width: 960px) and (max-width: 1279px) {
  .imagemPrincipal {
    width: 320px !important;
    height: 230px !important;
    margin-top: 90px !important;
    justify-content: center;
    margin-left: 80px !important;
    margin-right: -50px !important;
    align-items: center;
  }
}

.imagemPrincipal {
  margin-top: 35px;
  margin-left: 20px;
  margin-right: 20px;
  width: 504px;
  height: 381px;
}

@media screen and (min-width: 1280px) and (max-width: 1920px) {
  .imagemPrincipal {
    margin-left: 60px !important;
  }
}

@media screen and (max-width: 960px) {
  .imagemPrincipal {
    margin-left: 5px;
  }
}

@media screen and (max-width: 600px) {
  .imagemPrincipal {
    width: 320px !important;
    height: 230px !important;
  }
}

@media screen and (max-width: 600px) {
  .spacingImage1 {
    margin-top: -200px !important;
    margin-left: -40px !important;
    width:120px !important;
  }
}

@media screen and (max-width: 600px) {
  .spacingImage2 {
    margin-top: 110px !important;
    margin-left: 130px !important;
    width: 170px !important;
  }
}

.spacingImage1 {
  margin-top: -350px;
  margin-left: -40px;
  width: 183px;
}

@media screen and (min-width: 960px) and (max-width: 1279px) {
  .spacingImage1 {
    margin-top: -200px;
    margin-left: -50px;
    width:120px;
  }
}

.spacingImage2 {
  margin-top: 205px;
  margin-left: 240px;
  width: 253px;
}

@media screen and (min-width: 960px) and (max-width: 1279px) {
  .spacingImage2 {
    margin-top: 110px;
    margin-left: 140px;
    width: 170px;
  }
}

.secondCard {
  width: 500px;
}

.spacingContent {
  margin-top: -3px;
}

.cardIcons {
  border-radius: 12px;
  height: 40px;
  width: 40px;
}

.colorIcon {
  padding-left: 20px;
  padding-top: 14px;
  height: 17px;
  width: 17px !important;
}

.classTitle {
  margin-top: 12px;
  margin-bottom: 5px;
  font-size: 24px;
  font-weight: 600;
}

.blueCard {
  background-color: #161B33;
  width: 1128px;
  border-radius: 30px;
  margin-bottom: 15px;
}

@media screen and (max-width: 600px) {
  .blueCard {
    height: 600px;
  }
}

@media screen and (min-width: 601px) and (max-width: 960px) {
  .blueCard {
    height: 500px;
  }
}

@media screen and (min-width: 960px) {
  .blueCard {
    height: 262px;
  }
  .spacingCol1 {
    margin-top: 50px !important;
  }
  .spacingCol2 {
    margin-right: 50px !important;
  }
}

@media screen and (min-width: 961px) and (max-width: 995px) {
  .blueCard {
    height: 280px;
  }
}

.spacingCol1 {
  margin-top: 60px;
  margin-left: 50px;
  margin-right: 40px;
  color: #FFFFFF;
} 

.marginTitle1 {
  margin-left: 30%;
} 

@media screen and (max-width: 600px) {
  .marginTitle1 {
    margin-left: 10%;
  }
}

@media screen and (max-width: 960px) {
  .marginTitle1 {
    margin-left: 30%;
    margin-right: 30%;
  }
}

.fontSubtitle {
  font-size: 14px;
  font-weight: 600;
  margin-bottom: 20px;
}

.spacingCol2 {
  margin-top: 87px;
}

.emailInput {
  width: 408px;
}

.btnRegister {
  width: 408px;
  height: 40px;
  background-color: #4E42FF;
  color: #FFFFFF;
  font-weight: 600;
}

.principalDiv2 {
  margin-left: 90px;
  margin-bottom: 70px;
}

.spacingCardsIcons {
  width: 330px; 
}

.purpleCard {
  width: 1128px;
  height: 834px;
  border-radius: 30px;
  background-color: #4E42FF1A;
}

@media screen and (max-width: 600px) {
.purpleCard {
  height: 1850px;
}
.marginTitle {
  margin-left: 2px !important;
  padding-right: 50px !important;
}
.subCard2 {
  margin-top: 40px;
  width: 350px !important;
  height: 700px !important;
  }
  .emailInput3 {
  width: 250px !important;
  }
  .subCard1 {
    width: 350px !important;
    height: 700px !important;
  }
  .emailInput2 {
    width: 250px !important;
  }
  .spacingCols {
    width: 350px !important;
  }
  .styleFaq {
    margin-left: 5px;
  }
}

@media screen and (min-width: 601px) and (max-width: 960px) {
  .purpleCard {
    height: 1400px;
  }
  .marginTitle {
    margin-left: 20px !important;
    padding-right: 50px !important;
  }
  .subCard1 {
    margin-bottom: 30px;
  }
  .spacingCols {
    width: 350px !important;
  }
}

@media screen and (min-width: 961px) and (max-width: 1264px) {
  .marginTitle {
    margin-left: 20px !important;
    padding-right: 50px !important;
  }
  .subCard1 {
    width: 430px !important;
    height: 600px !important;
  }
  .subCard2 {
    width: 430px !important;
    height: 600px !important;
  }
  .emailInput2 {
    width: 330px !important;
  }
  .emailInput3 {
    width: 330px !important;
  }
}

@media screen and (min-width: 1265px) {
  .marginTitle {
    margin-left: 20px !important;
    padding-right: 50px !important;
  }
}


.marginTitle {
  margin-left: 25%;
  margin-top: 5%;
}

.subCard1 {
  width: 484px;
  height: 561px;
  margin-right: 30px;
  border-radius: 20px;
  padding-left: 50px;
  padding-right: 50px;
}

.priceFont {
  font-size: 40px;
  padding-left: 4px;
}

.emailInput2 {
  width: 388px;
  color: #161B331A;
  margin-top: 20px;
}

v-card-title {
  align-items: start;
}

.btnRegister2 {
  width: 388px;
  font-size: 14px;
  font-weight: 600;
}

.subCard2 {
  background-color:#161B33;
  width: 484px;
  height: 561px;
  margin-left: 30px;
  border-radius: 20px;
  padding-left: 50px;
  padding-right: 50px;
  color: #FFFFFF;
}

.emailInput3 {
  width: 388px;
  color: #ffffff;
  margin-top: 20px;
}

.styleFaq {
  font-size: 14px;
  font-weight: 600;
  margin-bottom: 10px;
}
.spacingCols {
  width: 644px;
}

.bold-title {
  font-weight: bold;
  font-size: 16px;
  margin-bottom: 6px;
  margin-top: 6px;
} 

.blueCard2 {
  background-color: #161B33;
  width: 1128px;
  height: 262px;
  border-radius: 30px;
  margin-top: 70px;
  margin-bottom: 15px;
}

.spacingCol3 {
  margin-top: 65px;
  margin-left: 60px;
  margin-right: 30px;
  color: #FFFFFF;
}

</style>