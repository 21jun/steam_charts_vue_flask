<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      clipped
      fixed
      app
    >
      <v-list dense>
        <router-link to="/TopGameChart">
          <v-list-tile @click="">
            <v-list-tile-action>
              <v-icon>list</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>데일리 TOP20 게임</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </router-link>
        <router-link to="/DetailPage">
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>search</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>게임 검색</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        </router-link>
        <router-link to="/TagSearch">
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>search</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>태그 조회</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        </router-link>
        <router-link to="/SingleGameinfo/570">
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>게임 상세정보</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        </router-link>
        <router-link to="/TagLists">
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>장르별 게임 선택</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        </router-link>
        <router-link to="/UserRecommand">
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>추천 게임</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        </router-link>
        <router-link to="/ReviewPage">
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>평점 조회</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        </router-link>
      </v-list>
    </v-navigation-drawer>
  <v-toolbar app></v-toolbar>
  <v-content>
    <v-container fluid>
      <router-view></router-view>
    </v-container>
  </v-content>
  <v-footer app></v-footer>
</v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: null
    }),
    props: {
      source: String
    }
  }
</script>