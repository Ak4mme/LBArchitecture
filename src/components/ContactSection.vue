<template>
  <section class="pb-8" id="contact">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="left">
            <v-col sm="4" class="hidden-xs-only">
              <v-img
                src="@/assets/img/sistemas.png"
                class="d-block ml-auto mr-auto"
                max-width="350px"
              />
            </v-col>
            <v-col cols="12" sm="5" class="v-margin-bottom white--text">
              <h1 class="font-weight-light display-1">Contate-nos</h1>
              <h3 class="font-weight-light mt-3">
                Teremos o maior prazer em responder quaisquer dúvidas e ajudar
                você a encontrar a melhor solução para sua empresa.
              </h3>
              <h3 class="font-weight-light mt-3">
                Solicite seu Orçamento
              </h3>
              <!-- <h3 class="font-weight-light mt-3">
                <v-icon>mdi-whatsapp</v-icon> (14) 99654-4820
              </h3> -->
              <br />
              <v-btn
                class="light-blue lighten-1 no-uppercase"
                href="https://9hkfh6zamps.typeform.com/to/D1cIPOH2"
                target="_blank"
                ><div class="mr-2"><v-icon>mdi-ballot</v-icon></div>
                Orçamento</v-btn
              >
            </v-col>
          </v-row>
          <v-row justify="left">
            <!-- EMAIL CONTACT FORM -->
            <!-- <v-col cols="12" sm="7">
              <v-form ref="form" v-model="valid" :lazy-validation="lazy">
                <v-text-field
                  v-model="name"
                  :rules="nameRules"
                  label="Nome"
                  required
                ></v-text-field>

                <v-text-field
                  v-model="email"
                  :rules="emailRules"
                  label="E-mail"
                  required
                ></v-text-field>

                <v-textarea
                  v-model="textArea"
                  :rules="textAreaRules"
                  label="Mensagem"
                  required
                />

                <v-btn
                  :disabled="!valid"
                  color="primary"
                  :dark="valid"
                  rounded
                  block
                  class="mt-3"
                  @click="submit"
                >
                  Enviar
                </v-btn>
              </v-form>
            </v-col> -->
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <div class="svg-border-waves text-white">
      <v-img src="~@/assets/img/borderWavesBlue.svg" />
    </div>
    <v-snackbar
      v-model="snackbar.enabled"
      timeout="3000"
      right
      top
      :color="snackbar.color"
    >
      {{ snackbar.text }}

      <template v-slot:action="{ attrs }">
        <v-btn text v-bind="attrs" @click="snackbar.enabled = false">
          Fechar
        </v-btn>
      </template>
    </v-snackbar>
  </section>
</template>

<style scoped>
#contact {
  background-image: url("~@/assets/img/bghero1.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 400px;
}
#contact .row {
  height: 100%;
  padding: 1%;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}
</style>

<script>
// import {db} from '@/main'

export default {
  data: () => ({
    icons: ["fa-facebook", "fa-twitter", "fa-linkedin", "fa-instagram"],
    valid: true,
    name: "",
    nameRules: [
      (v) => !!v || "O campo nome é obrigatório",
      (v) => (v && v.length >= 6) || "O nome precisa ter mais de 6 caracteres",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "O campo email é obrigatório",
      (v) => /.+@.+\..+/.test(v) || "O E-mail precisa ser válido",
    ],
    textArea: "",
    textAreaRules: [
      (v) => !!v || "O campo de texto é obrigatório",
      (v) => (v && v.length >= 10) || "Mínimo de 10 caracteres",
    ],
    lazy: false,
    snackbar: {
      enabled: false,
      text: "",
      color: "",
    },
  }),
  methods: {
    submit() {
      /*db.collection("contactData").add({
        name: this.name,
        email: this.email,
        message: this.textArea
      }).then(() => {
        this.snackbar.text = "Mensagem enviada com sucesso"
        this.snackbar.color = "success"
        this.snackbar.enabled = true
      }).catch(() => {
        this.snackbar.text = "Erro ao enviar mensagem"
        this.snackbar.color = "danger"
        this.snackbar.enabled = true
      })*/
    },
  },
};
</script>

<style scoped>
.no-uppercase {
  text-transform: none;
}
.v-margin-bottom {
  margin-bottom: 35px;
}
</style>