<template>
  <v-app>
    <!-- <v-app-bar
      app
      absolute
      :elevation="isScrolled ? 2 : 0"
      :color="isScrolled ? 'primary' : 'transparent'"
      :theme="isScrolled ? 'dark' : 'light'"
      class="app-bar-transition"
    >
    
      <v-spacer />

      <div class="d-none d-sm-flex">
        <v-btn
          v-for="item in menuItems"
          :key="item.title"
          :variant="'text'"
          class="mx-1"
          :class="{ 'active-link': item.active && !isScrolled }"
        >
          {{ item.title }}
        </v-btn>
      </div>

     Ícone de menu para mobile. A cor é controlada pela prop 'theme' da barra. -->
      <v-app-bar-nav-icon class="d-sm-none" @click="drawer = !drawer" />
  



    <!-- v-navigation-drawer para mobile. 'location' substitui 'right'/'left'. -->
    <v-navigation-drawer v-model="drawer" temporary location="right" class="d-sm-none">
      <v-list>
        <v-list-item v-for="item in menuItems" :key="item.title" link>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!-- App Bar -->
    <v-app-bar app absolute color="primary" dark >
      <v-app-bar-nav-icon @click="drawer = !drawer" class="d-sm-none" />
      <v-toolbar-title class="text-h6 text-sm-h5 font-weight-bold">Seminário IA </v-toolbar-title> <v-img max-width="20" src="../assets/logo.svg"/>
      <v-spacer></v-spacer>
      <v-btn v-for="item in menuItems" :key="item.title" :href="item.href" text class="mx-2 d-none d-sm-flex">
        {{ item.title }}
      </v-btn>
    </v-app-bar>

    <!-- Navigation Drawer (mobile) -->
    <!-- <v-navigation-drawer v-model="drawer" temporary class="d-sm-none">
      <v-list>
        <v-list-item v-for="item in menuItems" :key="item.title" :href="item.href" @click="drawer = false">
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->

    <!-- Main -->
    <v-main>
      <!-- Hero / Banner -->
      <v-parallax
        src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Mestre_%C3%81lvaro.jpg/1657px-Mestre_%C3%81lvaro.jpg"
        cover
        >
        <v-row
          class="justify-center align-center flex-column-reverse flex-md-row"
          style="height: 100%;"
        >
            <v-col
              cols="12"
              justify="center"
              align="center"
            >
                  <h2 style="color: white;" >24 e 25 de setembro de 2025</h2>
                  <h1 style="color: white;">SEMINÁRIO CAPIXABA DE APLICAÇÕES EM INTELIGÊNCIA ARTIFICIAL</h1>
                  <p style="color: white;">INSTITUTO FEDERAL DO ESPÍRITO SANTO - CAMPUS SERRA</p>
            </v-col>
        </v-row>
      </v-parallax>

      <!-- Sobre -->
      
        <v-container>
          
          <h2 class="text-h4 font-weight-bold mb-6 text-center">Sobre o Evento</h2>
          <p class="text-body-1" style="white-space: pre-line;">
            Para o Ifes, a organização do seminário reforça seu papel como instituição de referência no ensino, pesquisa e extensão. Ao promover um evento dessa magnitude, o Ifes não apenas demonstra seu comprometimento com a geração e disseminação de conhecimento, mas também fortalece sua conexão com a sociedade e com setores estratégicos, como a indústria, saúde, educação e gestão pública.

            A relevância técnico-científica do evento está no seu potencial para abordar desafios e oportunidades em áreas de grande impacto. A inteligência artificial possui aplicações transformadoras na indústria, otimizando processos produtivos e elevando a competitividade; no setor público, promovendo eficiência e transparência na gestão; na saúde, com avanços em diagnósticos e tratamentos personalizados; na educação, com ferramentas adaptativas e acessíveis; e em inúmeros outros campos.
          </p>
        </v-container>


      <!-- Dias do evento -->
      <section id="programacao" class="py-12">
        <v-container>
          <v-row>
            <v-col cols="12">
              <h2 class="text-h4 font-weight-bold mb-8 text-center">Programação</h2>
            </v-col>
            <v-col v-for="day in days" :key="day.title" cols="12" md="4" class="d-flex">
              <v-card elevation="4" class="flex-grow-1">
                <v-img :src="day.src" height="200px"></v-img>
                <v-card-title class="justify-center">{{ day.title }}</v-card-title>
                <v-card-text>{{ day.description }}</v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" class="text-center mb-4">
              <v-btn color="primary" large href="https://docs.google.com/forms/d/1aoIrMTHbns5TtFES8cQzgG0yYuUz1b59rAE6-1qU_zo/edit" target="_blank">
                Confirmar Presença
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </section>


      <!-- Palestrantes -->
        <v-container
          fluid
          style="background-color: #ffd700;"  
          height="100vh"
          align="center"
          justify="center"
        >
          <h2 class="text-h4 font-weight-bold mb-6 text-center">Palestrantes</h2>
          <v-carousel
            hide-delimiters
            height="350"
          >
            <v-carousel-item v-for="speaker in speakers" :key="speaker.name">
              <v-card class="mx-auto" max-width="300" elevation="4"
                @onClick="() => console.log(speaker.name)"
              >
                <v-img :src="speaker.src" height="250"></v-img>
                <v-card-title class="justify-center">{{ speaker.name }}</v-card-title>
                <v-card-text>{{ speaker.about }}</v-card-text>
              </v-card>
            </v-carousel-item>
          </v-carousel>
        </v-container>

      <!-- Local -->
      <section id="local" class="py-12">
        <v-container>
          <h2 class="text-h4 font-weight-bold mb-6 text-center">Local</h2>
          <v-row class="mb-4">
            <v-col cols="12" md="6">
              <p class="text-body-1 mb-2 font-weight-medium">IFES - CAMPUS SERRA</p>
              <p class="text-body-2">Av. dos Sabiás, 330 - Morada de Laranjeiras, Serra - ES, 29166-630</p>
              <p class="text-body-2">O Campus Serra está localizado às margens da Rodovia ES010, a uma distância aproximada de 20 km do aeroporto Eurico Sales...</p>
            </v-col>
            <v-col cols="12" md="6">
              <v-img src="https://via.placeholder.com/600x400?text=IFES+Serra" height="250"></v-img>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="6" sm="4" md="3" v-for="(social, i) in socials" :key="i">
              <v-btn :href="social.href" target="_blank" icon>
                <v-icon size="36">{{ social.icon }}</v-icon>
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </section>
    </v-main>

    <!-- Footer -->
    <v-footer padless color="primary" dark>
      <v-container class="py-4 text-center">
        © 2025 Seminário IA - Todos os direitos reservados
      </v-container>
    </v-footer>
  </v-app>
</template>

<script setup>
// import { ref } from 'vue'
import { ref, onMounted, onBeforeUnmount } from 'vue';

// No Vue 3, usamos 'ref' para criar variáveis reativas.
const drawer = ref(false);
const isScrolled = ref(false);

const menuItems = [
  { title: 'Página Inicial', href: '#' },
  { title: 'Programação', href: '#programacao' },
  { title: 'Inscrições', href: 'https://docs.google.com/forms/d/e/1FAIpQLSf...' },
  { title: 'Palestrantes', href: '#palestrantes' },
  { title: 'Local', href: '#local' }
]

const days = [
  {
    title: 'Dia 1',
    src: 'https://via.placeholder.com/600x400?text=Dia+1',
    description: 'Descrição breve sobre o dia 1.'
  },
  {
    title: 'Dia 2',
    src: 'https://via.placeholder.com/600x400?text=Dia+2',
    description: 'Descrição breve sobre o dia 2.'
  },
  {
    title: 'Dia 3',
    src: 'https://via.placeholder.com/600x400?text=Dia+3',
    description: 'Descrição breve sobre o dia 3.'
  }
]

const speakers = [
  {
    name: 'Alberto Ferreira',
    src: 'https://via.placeholder.com/300x300?text=Alberto+Ferreira',
    about: 'Sobre esta pessoa'
  },
  {
    name: 'Alexandre Chiavegatto',
    src: 'https://via.placeholder.com/300x300?text=Alexandre+Chiavegatto',
    about: 'Sobre esta pessoa'
  },
  {
    name: 'Anderson Soares',
    src: 'https://via.placeholder.com/300x300?text=Anderson+Soares',
    about: 'Sobre esta pessoa'
  },
  {
    name: 'Outro Nome',
    src: 'https://via.placeholder.com/300x300?text=Palestrante',
    about: 'Sobre esta pessoa'
  },
  {
    name: 'Mais um Palestrante',
    src: 'https://via.placeholder.com/300x300?text=Palestrante',
    about: 'CEO de uma empresa de tecnologia, especialista em IA.'
  }
]

const socials = [
  { icon: 'mdi-facebook', href: 'https://facebook.com' },
  { icon: 'mdi-twitter', href: 'https://twitter.com' },
  { icon: 'mdi-linkedin', href: 'https://linkedin.com' }
]
</script>

<style scoped>
.hero-section {
  background: url('https://via.placeholder.com/1600x600?text=Seminário+IA') center/cover no-repeat;
  color: white;
}
.hero-section h1 {
  font-size: 2.5rem;
  font-weight: bold;
}
.hero-text {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
}
</style>
