

<template>
    <v-app-bar>
      <v-toolbar-title>Seminário Capixaba de IA</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text href="index.html">Página Inicial</v-btn>
      <v-btn text href="programacao.html">Programação</v-btn>
      <v-btn text href="#inscricoes">Inscrições</v-btn>
      <v-btn text href="#">Palestrantes</v-btn>
      <v-btn text href="#">Local</v-btn>
    </v-app-bar>

    <!-- Hero Section -->
     <v-section>
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
                  <h2>24 e 25 de setembro de 2025</h2>
                  <h1>SEMINÁRIO CAPIXABA DE APLICAÇÕES EM INTELIGÊNCIA ARTIFICIAL</h1>
                  <p>INSTITUTO FEDERAL DO ESPÍRITO SANTO - CAMPUS SERRA</p>
            </v-col>
        </v-row>
      </v-parallax>
     </v-section>

    <!-- Seção Amarela -->
      <v-container
        fluid
        style="background-color: #ffd700; height: 100vh;"
        class="pa-0 ma-0 d-flex align-center justify-center"
      >
        <v-col cols="12"
          aling="center"
          justify="center"
        >
            <h2
              style="color: black;"
            >
              Ciclo de palestras - Paineis de discussão - Workshops
            </h2>

            <v-col cols="4">
              <v-card
                color="white"
              >
                <v-card-text>
                  <h2>Dia X</h2>
                </v-card-text>
              </v-card>
              <v-card-actions>
                <v-btn> Ação X</v-btn>
              </v-card-actions>
            </v-col>
        </v-col>
     </v-container>
    <section class="yellow-section full-screen" id="inscricoes">
        <div class="container">
            <h2>Ciclo de palestras - Paineis de discussão - Workshops</h2>
            <button class="btn">
                <a href="https://docs.google.com/forms/d/1aoIrMTHbns5TtFES8cQzgG0yYuUz1b59rAE6-1qU_zo/edit">
                    Confirmar Presença
                </a>
            </button>
            <div class="days-grid">
                <div class="day-item">
                    <h3>Dia 1</h3>
                    <img src="https://via.placeholder.com/300x200" alt="Dia 1">
                    <p>Descrição breve sobre o dia 1.</p>
                </div>
                <div class="day-item">
                    <h3>Dia 2</h3>
                    <img src="https://via.placeholder.com/300x200" alt="Dia 2">
                    <p>Descrição breve sobre o dia 2.</p>
                </div>
                <div class="day-item">
                    <h3>Dia 3</h3>
                    <img src="https://via.placeholder.com/300x200" alt="Dia 3">
                    <p>Descrição breve sobre o dia 3.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sidebar -->
    <section class="about-section">
        <div class="container">
            <div class="text-block">
                <h2>A realização do I Seminário de Inteligência Artificial do Estado do Espírito Santo</h2>
                <p>Para o Ifes, a organização do seminário reforça seu papel como instituição de referência no ensino, pesquisa e extensão. Ao promover um evento dessa magnitude, o Ifes não apenas demonstra seu comprometimento com a geração e disseminação de conhecimento, mas também fortalece sua conexão com a sociedade e com setores estratégicos, como a indústria, saúde, educação e gestão pública. O seminário também posiciona o campus Serra como um catalisador de inovações e um elo entre as demandas regionais e as tendências globais em IA.</p>
                <p>A relevância técnico-científica do evento está no seu potencial para abordar desafios e oportunidades em áreas de grande impacto. A inteligência artificial possui aplicações transformadoras na indústria, otimizando processos produtivos e elevando a competitividade; no setor público, promovendo eficiência e transparência na gestão; na saúde, com avanços em diagnósticos e tratamentos personalizados; na educação, com ferramentas adaptativas e acessíveis; e em inúmeros outros campos. Assim, o seminário permitirá a discussão de soluções inovadoras que podem ser implementadas diretamente no contexto capixaba, promovendo avanços significativos em diferentes setores.</p>
                <p>O impacto esperado inclui a ampliação da visibilidade da comunidade científica do Espírito Santo, a criação de redes de colaboração entre instituições locais e nacionais e o estímulo à formação de novos talentos em IA. Além disso, o seminário pode gerar benefícios de longo prazo, como o aumento do investimento em pesquisa e desenvolvimento na área e o fortalecimento de startups e empresas locais que utilizam tecnologias de IA.</p>
                <p>Outro aspecto fundamental do evento é sua abordagem interdisciplinar e multidisciplinar. A inteligência artificial é, por natureza, uma área que conecta conhecimentos de computação, matemática, estatística, engenharia, ciências humanas e sociais, entre outros campos. Essa característica permite que o seminário reúna especialistas de diferentes áreas para discutir soluções integradas e holísticas, capazes de enfrentar problemas complexos de maneira inovadora. Portanto, o I Seminário de Inteligência Artificial do Estado do Espírito Santo é uma oportunidade ímpar para alavancar o desenvolvimento científico e tecnológico local, conectando a comunidade acadêmica, os setores produtivos e a sociedade em geral em torno de uma temática estratégica e de grande relevância para o futuro.</p>
            </div>
            <img src="https://via.placeholder.com/400x300" alt="Imagem ilustrativa">
            <p class="image-caption">Legenda sobre o que os participantes podem esperar do evento</p>
        </div>
    </section>

    <!-- Seção de Palestrantes -->
    <section class="speakers-section full-screen" id="speakers">
        <div class="container" id="speakers-container" style="border-width: 5px; border-style: solid; margin: 5px;">
            <h2>Palestrantes</h2>
            <div class="speakers-grid" id="speakers-grid">
                <!-- Primeira linha de palestrantes -->
                <div class="speaker-item">
                    <img src="../assets/minibios/Alberto Ferreira/1517658465733.jpeg" alt="Palestrante 1">
                    <h3>[Alberto Ferreira]</h3>
                    <p>Sobre esta pessoa</p>
                </div>
                <div class="speaker-item">
                    <img src="../assets/minibio/Alexandre Chiavegatto/20250124_084651.jpg" alt="Palestrante 2">
                    <h3>[Alexandre Chiavegatto]</h3>
                    <p>Sobre esta pessoa</p>
                </div>
                <div class="speaker-item">
                    <img src="../assets/minibio/Anderson Soares/AndersonSoares.jpg" alt="Palestrante 3">
                    <h3>[Anderson Soares]</h3>
                    <p>Sobre esta pessoa</p>
                </div>
                <div class="speaker-item">
                    <img src="../assets/palestrantes/racas-cachorro-pequeno-3.jpg" alt="Palestrante 4">
                    <h3>[Nome]</h3>
                    <p>Sobre esta pessoa</p>
                </div>
            </div>
        </div>
    </section>

    <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
        <div class="carousel-inner">
            <div class="carousel-item active">
                <img src="../assets/palestrantes/buldogue_ingles-p.webp" alt="Palestrante 1">
            </div>
            <div class="carousel-item">
                <img src="../assets/palestrantes/imagem-vertical-de-foco-raso-de-um-filhote-de-cachorro-golden-retriever-fofo-sentado-em-um-gramado_181624-27259.avif" alt="Palestrante 2">
            </div>
            <div class="carousel-item">
                <img src="../assets/palestrantes/istockphoto-1482199015-612x612.jpg" alt="Palestrante 3">
            </div>
            <div class="carousel-item">
                <img src="../assets/palestrantes/racas-cachorro-pequeno-3.jpg" alt="Palestrante 4">
            </div>
        </div>
        <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
        </a>
    </div>

    <!-- Seção Local -->
    <aside class="location-sidebar full-screen">
        <div class="container">
            <h2>Local</h2>
            <h3>IFES - CAMPUS SERRA</h3>
            <p>
                Av. dos Sabiás, 330 - Morada de Laranjeiras, Serra - ES, 29166-630<br>
                O Campus Serra está localizado às margens da Rodovia ES010, a uma distância aproximada de 20 km do aeroporto Eurico Sales, principal porta de entrada de participantes e convidados do seminário. Duas vias principais conectam o aeroporto ao local do seminário: a Rodovia Norte/Sul e a BR101. O local do seminário pode ser facilmente acessado por automóvel, participantes que precisem utilizar o transporte público, contarão com uma malha do transporte público que facilitam o acesso ao Campus Serra, qualquer que seja a origem.
            </p>
            <div class="image-gallery">
                <img src="https://via.placeholder.com/400x300" alt="Imagem 1">
                <img src="https://via.placeholder.com/400x300" alt="Imagem 2">
            </div>
        </div>
    </aside>

    <!-- Rodapé -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <p>A realização do I Seminário de Inteligência Artificial do Estado do Espírito Santo [...] (texto completo aqui)</p>
                <div class="social-icons">
                    <a href="#"><img src="https://via.placeholder.com/30x30" alt="Facebook"></a>
                    <a href="#"><img src="https://via.placeholder.com/30x30" alt="Twitter"></a>
                    <a href="#"><img src="https://via.placeholder.com/30x30" alt="LinkedIn"></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script lang="ts" setup>
  //
</script>

