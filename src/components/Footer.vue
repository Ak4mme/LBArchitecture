<template>
  <v-footer dark padless>
    <v-card flat tile class="secondary white--text text-center">
      <v-card-text>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 white--text"
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text>
      <v-card-text class="white--text pt-0">
        Confira nosso trabalho em nossas redes sociais!
      </v-card-text>
      <v-divider></v-divider>
      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — FlowDev Sistemas e Consultoria. CNPJ:
        41.949.547/0001-15
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<style scoped>
.v-card {
  width: 100%;
}
</style>

<script>
export default {
  data: () => ({
    icons: [
      {
        text: "mdi-facebook",
        link: "https://www.facebook.com/flowdev.sistemas",
      },
      {
        text: "mdi-whatsapp",
        link: "https://api.whatsapp.com/send?phone=5514996544820",
      },
      {
        text: "mdi-instagram",
        link: "https://www.instagram.com/flowdev_sistemas/",
      },
      {
        text: "mdi-file-download",
        link: "https://cdn.discordapp.com/attachments/883081040829231164/890314709360844880/fav2.png",
      },
    ],
  }),
};
</script>
