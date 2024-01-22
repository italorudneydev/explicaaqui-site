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
            ></v-text-field> 
            <v-btn 
              rounded="xl" 
              class="registerButton"
            >CADASTRE-SE AGORA
            </v-btn>
          </div>
        </div>
        <div class="pa-5"> 
          <div class="principalImage mx-auto"> 
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

    <div class="biggerDivSpacing d-flex flex-column flex-md-column flex-lg-row mx-auto">
      <div class="mx-auto">
        <img class="dimensionImg" src="/src/assets/image-removebg.png"/>
      </div>
      <div class="mt-8"> 
        <h1 class="mx-auto mb-12">
          Aprenda, colabore com colegas e se desenvolva profissionalmente
        </h1>
        <!--Melhorar lógica-->
        <div class="flex-column d-flex mx-auto flex-md-row"> 
          <div 
            v-for="(variant, i) in variants.slice(0,2)" :key="i"
            class="spacingPrincipalCards d-flex justify-center"
          >
            <v-card class="spacingCardsIconsLearn" variant="flat">
              <v-card-item>
                <div>
                  <v-sheet
                    :height="40"
                    :width="40"
                    variant="tonal" 
                    :color="colors[i]"
                    rounded="lg"
                  >
                    <v-icon :color="colorIcon[i]" size="17" class="colorIcon">
                      {{ variant.icon }}
                    </v-icon>
                  </v-sheet>
                  <h6 class="classTitle">{{ variant.title }}</h6>
                  <div>{{ variant.description }}</div>
                </div>
              </v-card-item>
              <v-divider
                class="mt-7 d-md-none d-xl-none d-lg-none"
                :thickness="2"
              ></v-divider>
            </v-card>
          </div>
        </div>
        <div class="flex-column d-flex mx-auto flex-md-row"> 
          <div 
            v-for="(variant, i) in variants.slice(2,4)"
            :key="i"
            class="spacingPrincipalCards d-flex justify-center"
          >
            <v-card class="spacingCardsIconsLearn" variant="flat">
              <v-card-item>
                <div>
                  <v-sheet
                    :height="40"
                    :width="40"
                    variant="tonal" 
                    :color="colors[i]"
                    rounded="lg"
                  >
                    <v-icon :color="colorIcon[i]" size="17" class="colorIcon">
                      {{ variant.icon }}
                    </v-icon>
                  </v-sheet>
                  <h6 class="classTitle">{{ variant.title }}</h6>
                  <div>{{ variant.description }}</div>
                </div>
              </v-card-item>
              <v-divider
                class="mt-7 d-md-none d-xl-none d-lg-none"
                :thickness="2"
              ></v-divider>
            </v-card>
          </div>
        </div>
      </div>
    </div>

    <div class="d-flex justify-center mt-12">
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
            <v-btn rounded="xl" class="mx-auto btnRegister">CADASTRE-SE AGORA </v-btn>
          </div>
        </div>
      </v-card>
    </div>
    
    <div class="mt-10">
      <div>
        <h1 class="marginTitle1 d-flex mb-12">
          Comece sua jornada no Explica Aqui agora mesmo!
        </h1>
        <div class="flex-column d-flex justify-center mx-auto flex-md-row">
          <div
            v-for="(itens, x) in itens2"
            :key="x"
            class="spacingPrincipalCards d-flex justify-center"
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

    <div class="d-flex justify-center mt-12">
      <v-card variant="flat" class="purpleCard justify-center text-center">
        <v-col class="marginTitle">
          <h1>Escolha o plano que melhor atende às suas necessidades</h1>
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

    <div class="d-flex flex-column flex-md-row justify-center mt-12 mx-auto commonQuestions">
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

    <div class="d-flex justify-center mt-12">
      <v-card class="blueCard2">
        <div class="d-flex justify-center flex-column flex-md-row">
          <div class="spacingCol3">
            <p class="fontSubtitle"><v-icon class="mr-2">mdi-wifi</v-icon>ACESSO ILIMITADO</p>
            <h1>Dê o primeiro passo em direção ao seu desenvolvimento profissional.</h1>
          </div>
          <div class="mx-auto spacingCol2">
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

.principalDiv {
  margin-left: 10%;
  margin-right: 10%;
}

.dimensionImg {
  width: 400px;
  height: 600px;
}

.principalImage {
  margin-top: 35px;
  margin-bottom: 150px;
  margin-left: 20px;
  margin-right: 20px;
  width: 504px;
  height: 381px;
}

.biggerDivSpacing {
  margin-top: 20px;
  margin-left: 20% !important;
  margin-right: 18% !important;
}

.spacingImage1 {
  margin-top: -350px;
  margin-left: -40px;
  width: 183px;
}

.spacingImage2 {
  margin-top: 205px;
  margin-left: 240px;
  width: 253px;
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

.spacingCol1 {
  margin-top: 60px;
  margin-left: 50px;
  margin-right: 40px;
  color: #FFFFFF;
} 

.marginTitle1 {
  margin-left: 25%;
  margin-right: 30%;
}

/*específico */ 
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

.spacingCardsIconsLearn {
  width: 400px; 
}

.purpleCard {
  width: 1128px;
  height: 834px;
  border-radius: 30px;
  background-color: #4E42FF1A;
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
  border-radius: 30px;
  margin-bottom: 30px;
}

.spacingCol3 {
  margin-top: 60px;
  margin-left: 50px;
  margin-right: 40px;
  color: #FFFFFF;
}
/*breakpoints */
@media screen and (max-width: 599px) {
  .principalCard {
    height: 1000px;
  }
  .principalImage {
    width: 320px !important;
    height: 230px !important;
    padding-left: 20px;
  }
  .spacingImage1 {
    margin-top: -200px !important;
    margin-left: -40px !important;
    width:120px !important;
  }
  .spacingImage2 {
    margin-top: 110px !important;
    margin-left: 130px !important;
    width: 170px !important;
  }
  .dimensionImg {
    width: 330px !important;
    height: 436px !important;
  }
  .blueCard {
    height: 600px;
  }
  .blueCard2 {
    height: 600px;
  }
  .marginTitle1 {
    margin-left: 4% !important;
    margin-right: 4% !important;
  }
  .spacingTitle {
    margin-left: 5% !important;
    margin-right: 5% !important;
  }
  .spacingPrincipalCards {
    margin-left: 4%;
    margin-right: 4%;
  }
  .titleLearn {
    margin-left: 30px !important;
    margin-right: 30px !important;
  }
  .principalDiv {
    margin-left: 10px ;
    margin-right: 10px;
  }
  .purpleCard {
    height: 1750px !important;
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
  .btnRegister {
    width: 295px;
  }
  .emailInput {
    width: 295px;
  }
  .spacingCol1 {
    margin-left: 30px;
  } /* margem para conteúdo caber dentro do card */
  .commonQuestions {
    padding-left: 20px;
  }
  .biggerDivSpacing {
    margin-left: 10% !important;
    margin-right: 10% !important;
  }
}

@media screen and (min-width: 600px) and (max-width: 959px) {
  .marginTitle1 {
    margin-left: 15%;
    margin-right: 15%;
  }
  .spacingTitle {
    margin-left: 20%;
    margin-right: 15%;
  }
  .dimensionImg {
    width: 320px !important;
    height: 436px !important;
  }
  .blueCard {
    height: 500px;
  }
  .blueCard2 {
    height: 500px;
  }
  .principalImage {
    margin-left: 5px;
  }
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
    width: 450px !important;
  }
  .principalCard {
    max-width: 150%;
    height: 1000px;
  }
  .spacingCol {
    margin-left: 5%;
    margin-right: 5%;
  }
  .commonQuestions {
    margin-left: 15px;
  }
  .titleLearn {
    margin-left: 100px !important;
    margin-right: 10px !important;
  }
}

@media screen and (min-width: 960px) and (max-width: 1279px) {
  .principalImage {
    width: 320px !important;
    height: 230px !important;
    margin-top: 90px !important;
    justify-content: center;
    margin-left: 80px !important;
    margin-right: -50px !important;
    align-items: center;
  }
  .dimensionImg {
    width: 330px !important;
    height: 436px !important;
    margin-top: 50px;
    margin-right: 50px;
  }
  .spacingImage1 {
    margin-top: -200px;
    margin-left: -50px;
    width:120px;
  }
  .spacingImage2 {
    margin-top: 110px !important;
    margin-left: 140px !important;
    width: 170px !important;
  }  
  .spacingCol {
    margin-left: 8%;
    margin-right: 8%;
  }
  .blueCard {
    height: 262px;
  }
  .blueCard2 {
    height: 280px;
  } /* texto desce quando atinge x dimensão */
  /* 
  (min-width: 960px) and (max-width: 995px)
  .blueCard {
    height: 280px;
  }
  .blueCard2 {
    height: 280px;
  }
  */
  .spacingCol1 {
    margin-top: 50px !important;
    margin-right: 10px;
  }
  .spacingCol2 {
    margin-right: 50px !important;
  }
  .spacingCol3 {
    margin-top: 50px !important;
  }
  .spacingCardsIconsLearn {
    width: 280px; 
  }
  .subCard2 {
    padding-left: 45px;
  }
  .commonQuestions {
    padding-left: 20px;
  } 
  .titleLearn {
    margin-left: 220px !important;
    margin-right: 100px !important;
  }
}

@media screen and (min-width: 959px) and (max-width: 1720px) {
  .principalCard {
    max-width: 150%;
    max-width: 150%;
    height: 500px;
  }
}

@media screen and (min-width: 1280px) and (max-width: 1920px) {
  .spacingCol {
    margin-left: 5%;
    margin-right: 5%;
  }
  .spacingCardsIconsLearn {
    width: 280px; 
  }
  .principalImage {
    margin-right: 0px !important;
  }
  .titleLearn {
    margin-left: 150px !important;
    margin-right: 100px !important;
  }
  .dimensionImg {
    margin-top: 50px;
    margin-right: 50px;
  }
} 

@media screen and (min-width: 1600px) and (max-width: 1920px) {
  .divText {
    margin-left: 10%;
    margin-right: 12%;
  }
}

@media screen and (min-width: 960px) and (max-width: 1264px) {
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
  .spacingCol3 {
    margin-top: 30px;
    margin-bottom: 30px;
  }
  .spacingCol2 {
    margin-top: 50px;
    margin-bottom: 30px;
    padding-right: 20px;
  }
  .spacingCol1 {
    margin-top: 30px;
    margin-bottom: 30px;
  }
}

</style>