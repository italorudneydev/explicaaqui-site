<template>
    <v-main>
      <v-card style="z-index: auto;" height="72px">
        <div class="justify-center d-flex spacingPrincipal">
          <div class="me-auto d-none d-md-flex">
            <v-img 
              :width="200"
              :height="38"
              src="/src/assets/Logo-padrao.png"
            ></v-img>
          </div>
          <div class="d-none d-md-flex">
            <v-btn 
                variant="text"
                v-for="(item, index) in items"
                :key="index"
                @click="redirectToLink(item.link)"
            >{{ item.title }}</v-btn>
            <v-btn variant="outlined" rounded="xl">Cadastre-se agora</v-btn>
          </div>

          <!-- Tela menor -->
          <v-navigation-drawer class="w-100" temporary v-model="drawer" location="right">
            <v-list class="d-flex mx-auto">
                <v-img
                    src="/src/assets/Logo-icone.png"
                    :height="60"
                    class="d-flex"
                ></v-img>
                <v-spacer></v-spacer>
                <v-btn
                    variant="text"
                    class="mt-3"
                    @click.stop="drawer = !drawer"
                >
                    <v-icon size="30">mdi-window-close</v-icon>
                </v-btn>
            </v-list>

            <v-divider class="mb-2"></v-divider>
            <v-list
                v-for="(item, index) in items"
                :key="index"
            >
                <v-list-item
                @click="redirectToLink(item.link)"
                class="mb-4">
                    {{ item.title }}
                </v-list-item>
                <v-divider :thickness="2"></v-divider>
            </v-list>
        </v-navigation-drawer>
                
            <div class="d-sm-flex mx-auto d-md-none">
                <v-img 
                :width="200"
                :height="38"
                src="/src/assets/Logo-icone.png"
                class="teste"
                ></v-img> <!-- logo pequena-->
            </div>
  
            <v-spacer class="d-sm-flex d-md-none"></v-spacer>

            <v-btn variant="outlined" rounded="xl" class="d-sm-flex d-md-none">Cadastre-se agora</v-btn>
            <v-btn class="iconMenu d-sm-flex d-md-none" @click.stop="drawer = !drawer" variant="icon">
                <v-icon size="30">mdi-menu</v-icon>
            </v-btn>
                
        </div>
   
       
      </v-card>
    </v-main>
  </template>
  
<script>
    export default {
      data() {
        return {
          drawer: null,
          rail: true,
          items: [
            { title: 'BENEFÍCIOS', link: '/https://pictogrammers.com/library/mdi/icon/window-close/' },
            { title: 'COMO FUNCIONA', link: '/link-2' },
            { title: 'PLANOS', link: '/link-3' },
            { title: 'FAQ', link: '/link-4' },
            ],
        }
      },
    }
</script>
  
  
<style>
  
.header {
    background-color: #4E42FF0D;
    height: 200px !important;
}
.drawer-on-top {
    z-index: 1; /* Adjust as needed */
}
 
  @media screen and (max-width: 959px) {
    .spacingPrincipal {
      margin-top: 15px;
    }
  }
  
  @media screen and (min-width: 960px) {
    .spacingPrincipal {
      margin-left: 150px;
      margin-right: 10%;
      margin-top: 18px;
    }
  }
  
.iconMenu {
margin-right: 10px;
margin-top: 2px;
}

.imageNavigation {
margin-left: -20px;
}

.testee {
margin-right: 50%;
margin-left: 10px;
}

.teste {
padding-right: -20px;
}

</style>
  