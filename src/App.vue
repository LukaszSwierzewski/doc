<template>
  <div id="app">
    <v-app id="inspire">
      <v-navigation-drawer class="elevation-10" v-model="drawer" app>
        <v-list class="menu" dense>
          <v-img class="logo" src="./assets/logos.png" contain></v-img>
          <v-divider></v-divider>
          <v-list-item to="/">
            <v-list-item-action> </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>Wstęp</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item to="/dokumentacja">
            <v-list-item-action> </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>Dokumentacja</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item to="/dokumentacja">
            <v-list-item-action> </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>Użyteczne programy</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-divider></v-divider>
          <h4 class="menu__heading">Panel sport-max</h4>
          <v-list-item to="/dokumentacja">
            <v-list-item-action> </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>Jak używać panelu</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item to="/dokumentacja">
            <v-list-item-action> </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>Dodawanie produktów</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item to="/dokumentacja">
            <v-list-item-action> </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title><strong>HTML5</strong></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-expansion-panels>
            <v-expansion-panel>
              <v-expansion-panel-header
                >Szablony aukcyjne</v-expansion-panel-header
              >
              <v-expansion-panel-content padding="0px" class="menu__expansion">
                <v-list-item to="/dokumentacja">
                  <v-list-item-action> </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title>Szablon 1</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item to="/dokumentacja">
                  <v-list-item-action> </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title>Szablon 2</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item to="/dokumentacja">
                  <v-list-item-action> </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title>Szablon 3</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
          <v-expansion-panels>
            <v-expansion-panel>
              <v-expansion-panel-header
                >Artykuły na bloga</v-expansion-panel-header
              >
              <v-expansion-panel-content padding="0px" class="menu__expansion">
                <v-list-item to="/dokumentacja">
                  <v-list-item-action> </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title>Wstępne ustawienia</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item to="/dokumentacja">
                  <v-list-item-action> </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title>Zdjęcia, buttony</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item to="/dokumentacja">
                  <v-list-item-action> </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title
                      >Kontent artykułu - HTML</v-list-item-title
                    >
                  </v-list-item-content>
                </v-list-item>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-list>
      </v-navigation-drawer>

      <v-app-bar app color="indigo" dark>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title>Dokumentacja sport-max</v-toolbar-title>
      </v-app-bar>

      <v-content>
        <v-container fluid fill-height>
          <v-layout align-center justify-center>
            <router-view></router-view>
          </v-layout>
        </v-container>
      </v-content>
      <v-footer color="indigo" app>
        <span class="white--text">&copy; 2019</span>
      </v-footer>
    </v-app>
  </div>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: null
  }),
  mounted() {}
};
</script>
<style lang="scss">
.logo {
  padding: 20px;
  width: 90%;
  margin: 0 auto;
}
.menu {
  &__heading {
    margin-left: 20px;
    padding: 10px 0px;
  }
}
.menu__expansion > div {
  padding: 0px 0px 16px;
}
</style>
