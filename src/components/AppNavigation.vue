<template>
  <span>
    <v-navigation-drawer app v-model="drawer" class="grey darken-4" dark disable-resize-watcher>
      <v-list>
        <template v-for="(item, index) in items">
          <v-list-tile :key="index">
            <v-list-tile-content>
              <v-btn color="amber darken-1" @click="drawer = !drawer">{{item.title}}</v-btn>
            </v-list-tile-content>
          </v-list-tile>
          <v-divider :key="`divider-${index}`"></v-divider>
        </template>
      </v-list>
    </v-navigation-drawer>

    <v-toolbar color="amber darken-1">
      <v-app-bar-nav-icon @click="drawer = !drawer" class="hidden-md-and-up"></v-app-bar-nav-icon>

      <v-spacer class="hidden-md-and-down"></v-spacer>
      <v-img class="mx-2" src="@/assets/logo.png" max-height="80" max-width="80" contain></v-img>
      <v-toolbar-title>{{appTitle}}</v-toolbar-title>
      <v-spacer class="hidden-md-and-down"></v-spacer>
      <v-dialog dark v-model="registerDialog" persistent max-width="400px">
        <template v-slot:activator="{ on }">
          <v-btn text v-on="on">
            <v-icon>mdi-account-key</v-icon>S'Inscrire
          </v-btn>
        </template>
        <v-card>
          <v-card-title>
            <span color="amber darken-1" class="headline">Inscription</span>
          </v-card-title>
          <v-card-text>
            <v-container>
              <v-row>
                <v-col cols="12" md="12">
                  <v-text-field
                    clearable
                    label="Nom d'utilisateur *"
                    prepend-icon="mdi-account"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="12">
                  <v-text-field clearable prepend-icon="mdi-key" label="Mot de passe *" required></v-text-field>
                </v-col>
                <v-col cols="12" md="12">
                  <v-text-field clearable prepend-icon="mdi-email" label="E-Mail *" required></v-text-field>
                </v-col>
                <v-col cols="12" md="12">
                  <v-text-field clearable prepend-icon="mdi-phone" label="Numéro de téléphone "></v-text-field>
                </v-col>
              </v-row>
            </v-container>
            <small>*champs requis</small>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="amber darken-1" light @click="registerDialog = false">S'Inscrire</v-btn>
            <v-btn color="amber darken-1" text @click="registerDialog = false">Annuler</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>

      <v-dialog dark v-model="loginDialog" persistent max-width="400px">
        <template v-slot:activator="{ on }">
          <v-btn color="grey darken-4" dark v-on="on">
            <v-icon>mdi-account-key</v-icon>Se Connecter
          </v-btn>
        </template>
        <v-card>
          <v-card-title>
            <span color="amber darken-1" class="headline">Connexion</span>
          </v-card-title>
          <v-card-text>
            <v-container>
              <v-row>
                <v-col cols="12" md="12">
                  <v-text-field
                    clearable
                    label="Nom d'utilisateur *"
                    prepend-icon="mdi-account"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="12">
                  <v-text-field
                    :type="'password'"
                    clearable
                    prepend-icon="mdi-key"
                    label="Mot de passe *"
                    required
                  ></v-text-field>
                </v-col>
              </v-row>
            </v-container>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="amber darken-1" light @click="loginDialog = false">Se Connecter</v-btn>
            <v-btn color="amber darken-1" text @click="loginDialog = false">Annuler</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-toolbar>
  </span>
</template>

<script>
export default {
  name: "AppNavigation",

  components: {},

  data() {
    return {
      appTitle: "Queezzz",
      drawer: false,
      loginDialog: false,
      registerDialog: false,
      items: [{ title: "Menu" }, { title: "Sign In" }, { title: "Join" }]
    };
  }
};
</script>
<style scoped>
.logo {
  width: 28px;
  height: 28px;
}
</style>