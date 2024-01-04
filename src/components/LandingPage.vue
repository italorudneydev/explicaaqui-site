<template>
  <v-app>
      <v-card variant="flat" class="principalCard">
        <div class="principalDiv d-flex justify-center align-center h-100">
          <div class="spacing"> 
            <p class="titlename"><v-icon>mdi-flash</v-icon>PLATAFORMA EXCLUSIVA</p>
            <h1 class="mt-4 mb-5">Conecte-se com outros servidores públicos e amplie seu conhecimento</h1>
            <p class="mr-3">
              Com o Explica Aqui, você tira suas dúvidas, aprende com os melhores especialistas e constrói uma rede de contatos para se manter atualizado e avançar na carreira.
            </p>
            <div class="d-flex mt-4 justify-center">
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
          <div class="imagemPrincipal"> 
            <v-card variant="flat" rounded="xl">
              <v-img
                :width="504"
                :height="381"
                aspect-ratio="16/9"
                cover
                src="/src/assets/tablet-digital-pode-resolver-o-problema 1.png"
              ></v-img>
            </v-card>
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
      </v-card>

      <div class="principalDiv d-flex justify-center align-center">
        <div>
          <img 
            src="/src/assets/image-removebg.png"
            :width="472"
            :height="600"
          >
        </div>
        <div class="mt-15">
          <h1 class="ml-14">Aprenda, colabore com colegas e se desenvolva profissionalmente</h1>
            <v-row align="center" justify="center">
              <v-col v-for="(variant, i) in variants" :key="i" cols="auto">
                <v-card class="secondCard" variant="flat">
                  <v-card-item>
                    <div>
                      <v-sheet
                        class="cardIcons"
                        variant="tonal"
                        :color="colors[i]" 
                      >
                        <v-icon 
                          :color="colorIcon[i]" 
                          size="17" 
                          class="colorIcon" 
                        > {{ variant.icon }}
                        </v-icon>
                      </v-sheet>
                      <h6 class="classTitle">{{ variant.title }}</h6>
                      <div>{{ variant.description }}</div>
                    </div>
                  </v-card-item>
                </v-card>
              </v-col>
            </v-row>
        </div>
      </div>
      <div class="d-flex justify-center">
        <v-card class="blueCard">
          <div class="d-flex justify-center">
            <div class="spacingCol1">
              <p class="fontSubtitle"><v-icon class="mr-2">mdi-cellphone-link</v-icon>DISPONÍVEL EM TODAS AS PLATAFORMAS</p>
              <h1>Junte-se à maior comunidade de servidores públicos do Brasil.</h1>
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
      <div class="principalDiv2 mt-10 d-flex justify-center">
        <div>
          <v-col cols="5">
            <h1>Comece sua jornada no Explica Aqui agora mesmo!</h1>
          </v-col>

          <v-col cols="4"></v-col>
        
          <div class="d-flex">
              <div v-for="(itens, x) in itens2" :key="x">
                <v-card class="spacingCardsIcons" variant="flat">
                  <v-card-item>
                    <div>
                      <v-sheet variant="tonal" :color="colors2[x]" :height="40" :width="40" rounded="lg">
                        <v-icon 
                          :color="colorIcon2[x]" 
                          size="17" 
                          class="colorIcon"
                        >{{ itens.icon2 }}
                        </v-icon>
                      </v-sheet>
                      <h6 class="classTitle">{{ itens.title2 }}</h6>
                      <div>{{ itens.description }}</div>
                      <div class="mt-4">{{ itens.description2 }}</div>
                    </div>
                  </v-card-item>
                </v-card>
              </div>
          </div>
        </div>
      </div>
      <div class="d-flex justify-center">
        <v-card variant="flat" class="purpleCard justify-center text-center">
          <v-col cols="6" class="marginTitle">
            <h1>
              Escolha o plano que melhor atende às suas necessidades
            </h1>
          </v-col>
          <div class="d-flex justify-center mt-10">
            <v-card 
              align="start" 
              variant="flat" 
              class="subCard1"
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


            <v-card align="start" variant="flat" class="subCard2">
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

      <div class="d-flex justify-center mt-12">
        <div>
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
        { title: 'O que é o Explica Aqui?', expandedText: 'Conteúdo do Item 1' },
        { title: 'Quais são os benefícios do Explica Aqui?', expandedText: 'Conteúdo do Item 2' },
        { title: 'Como posso me cadastrar no Explica Aqui?', expandedText: 'Conteúdo do Item 2' },        
        { title: 'Quais são os planos disponíveis no Explica Aqui?', expandedText: 'Conteúdo do Item 3' },
        { title: 'Qual a diferença entre respostas verificadas e não verificadas?', expandedText: 'Conteúdo do Item 4' },
        { title: 'Posso trocar do Plano Gratuito para o Premium a qualquer momento?', expandedText: 'Conteúdo do Item 5' },
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
}

.principalDiv {
  margin-left: 20%;
  margin-right: 20%;
  margin-bottom: 10%;
}

.spacing {
  margin-right: 15%;
}

.titlename {
  font-weight: 600;
  font-size: 14px;
}

.insertButton {
  width: 219px !important;
  height: 40px;
  margin-right: 12px;
  margin-top: 15px;
  margin-bottom: 40px;
  font-weight: 600 !important;
}

.registerButton {
  background-color: #161B33 !important;
  color: white !important;
  width: 199px;
  height: 40px;
  margin-top: 15px;
  margin-bottom: 40px;
  font-weight: 600 !important;
  font-size: 13px;
}

.imagemPrincipal {
  margin-top: 35px;
  margin-left: 20px;
  margin-right: 20px;
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

.secondCard {
  margin-left: 5px;
  max-width: 280px;
  margin: auto;
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
  margin-bottom: 12px;
  font-size: 24px;
  font-weight: 600;
}


.blueCard {
  background-color: #161B33;
  width: 1128px;
  height: 262px;
  border-radius: 30px;
  margin-top: -130px;
  margin-bottom: 15px;
}

.spacingCol1 {
  margin-top: 60px;
  margin-left: 60px;
  margin-right: 80px;
  color: #FFFFFF;
}

.fontSubtitle {
  font-size: 14px;
  font-weight: 600;
  margin-bottom: 20px;
}

.spacingCol2 {
  margin-top: 87px;
  margin-right: 50px;
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
  margin-right: 85px;
  width: 330px; 
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
  margin-left: 7px;
  margin-bottom: 10px;
}
.spacingCols {
  margin-left: 90px;
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