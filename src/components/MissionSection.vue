<template>
  <section id="mission">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col sm="4" class="hidden-xs-only">
              <v-img
                src="@/assets/img/ill2.svg"
                class="d-block ml-auto mr-auto"
                max-width="350px"
              />
            </v-col>
            <v-col cols="12" sm="8" class="white--text text-left">
              <h1 class="font-weight-light bold display-1 mb-2">
                Sobre a FlowDev
              </h1>
              <h3 class="font-weight-light">
                Somos uma empresa de desenvolvimento de aplicações web e
                consultoria situada em Botucatu - SP formada por quatro
                tecnólogos graduados em Análise e Desenvolvimento de Sistemas.
                <br /><br />
                Com muita determinação a FlowDev tem desenvolvido soluções de
                alto desempenho utilizando tecnologias inovadoras com baixo
                custo, conquistando cada vez mais o mercado do interior
                paulista.
              </h3>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#mission {
  background-image: url("~@/assets/img/bgDownload.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 500px;
}

#mission .container,
#mission .row {
  height: 100%;
}
</style>