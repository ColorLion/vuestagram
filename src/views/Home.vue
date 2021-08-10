<template>
  <div class="home">
    <v-container fluid class="mt-4">
      <v-row>
        <v-col cols="12" sm="3">
          <v-card color="#23252D" elevation="5">
            <v-row>
              <v-col cols="12" sm="6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <div>
                      <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">도희가 깬거</v-list-item-subtitle>
                      <v-icon color="grey" x-large>fas fa-user</v-icon>
                    </div>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
              <v-col cols="12" sm="6">
                <v-list-item three-line>
                  <v-list-item-content class="text-right">
                    <div>
                      <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">742,824</v-list-item-subtitle>
                      <v-list-item-subtitle class="grey--text" style="font-size: 11px">CHANGE TO</v-list-item-subtitle>
                      <v-list-item-subtitle class="grey--text mb-5" style="font-size: 11px">PREVIOUS MONTH</v-list-item-subtitle>
                      <v-icon color="green" class="mt-2 mr-2">fas fa-sort-up</v-icon>
                      <span class="green-text">+20,592</span><br>
                      <span class="green-text">(2.16%)</span>
                    </div>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="3">
          <v-card color="#23252D" elevation="5">
            <v-row>
              <v-col cols="12" sm="6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <div>
                      <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">도희가 실패한거</v-list-item-subtitle>
                      <v-icon color="grey" x-large>fab fa-pagelines</v-icon>
                    </div>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
              <v-col cols="12" sm="6">
                <v-list-item three-line>
                  <v-list-item-content class="text-right">
                    <div>
                      <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">914,175</v-list-item-subtitle>
                      <v-list-item-subtitle class="grey--text" style="font-size: 11px">CHANGE TO</v-list-item-subtitle>
                      <v-list-item-subtitle class="grey--text mb-5" style="font-size: 11px">PREVIOUS MONTH</v-list-item-subtitle>
                      <v-icon color="red" class="mt-2 mr-2">fas fa-sort-down</v-icon>
                      <span class="green-text">-21,724</span><br>
                      <span class="green-text">(0.12%)</span>
                    </div>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="3">
          <v-card color="#23252D" elevation="5">
            <v-row>
              <v-col cols="12" sm="6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <div>
                      <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">Advanced Lv.1</v-list-item-subtitle>
                      <v-icon color="grey" x-large>fas fa-chart-pie</v-icon>
                    </div>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
              <v-col cols="12" sm="6">
                <v-list-item three-line>
                  <v-list-item-content class="text-right">
                    <div>
                      <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">415,721</v-list-item-subtitle>
                      <v-list-item-subtitle class="grey--text" style="font-size: 11px">CHANGE TO</v-list-item-subtitle>
                      <v-list-item-subtitle class="grey--text mb-5" style="font-size: 11px">PREVIOUS MONTH</v-list-item-subtitle>
                      <v-icon color="green" class="mt-2 mr-2">fas fa-sort-up</v-icon>
                      <span class="green-text">+12,491</span><br>
                      <span class="green-text">(4.12%)</span>
                    </div>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="3">
          <v-card color="#23252D" elevation="5">
            <v-row>
              <v-col cols="12" sm="6">
                <v-list-item three-line>
                  <v-list-item-content>
                    <div>
                      <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">흐에</v-list-item-subtitle>
                      <v-icon color="grey" x-large>fas fa-sort-up</v-icon>
                    </div>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
              <v-col cols="12" sm="6">
                <v-list-item three-line>
                  <v-list-item-content class="text-right">
                    <div>
                      <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">274,762</v-list-item-subtitle>
                      <v-list-item-subtitle class="grey--text" style="font-size: 11px">CHANGE TO</v-list-item-subtitle>
                      <v-list-item-subtitle class="grey--text mb-5" style="font-size: 11px">PREVIOUS MONTH</v-list-item-subtitle>
                      <v-icon color="green" class="mt-2 mr-2">fas fa-sort-up</v-icon>
                      <span class="green-text">+16,592</span><br>
                      <span class="green-text">(7.11%)</span>
                    </div>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="7">
          <v-card color="#23262D">
            <v-app-bar color="rgba(0,0,0,0)" flat>
              <v-toolbar-title class="grey--text title">이달의 챔피언</v-toolbar-title>
              <v-spacer></v-spacer>
              <v-text-field
                v-model="search"
                append-icon="mdi-magnify"
                label="Search"
                single-line
                hide-details
              ></v-text-field>
              <v-chip class="ma-2" color="grey darken-1" pill>April 18
                <v-icon right small color="cyan">
                  fas fa-chevron-circle-down
                </v-icon>
              </v-chip>
            </v-app-bar>
            <v-data-table :headers="headers" :items="desserts" :search="search" class="dattab">
              <template v-slot:item.glutenfree="{ item }">
                <v-simple-checkbox v-model="item.glutenfree" color="cyan"></v-simple-checkbox>
              </template>
              <template v-slot:item.rating="{ item }">
                <v-rating v-model="item.rating" background-color="pink lighten-3" color="pink"></v-rating>
              </template>
              <template v-slot:item.action="">
                <v-icon small>mdi-pencil</v-icon>
              </template>
            </v-data-table>
          </v-card>
        </v-col>
        <v-col cols="12" sm="5">
          <v-card color="#23262D">
            <v-app-bar color="rgba(0,0,0,0)" flat>
              <v-toolbar-title class="grey--text title">
                Support ticket
              </v-toolbar-title>
            </v-app-bar>
            <v-list three-line class="mt-n5" color="#23262D">
              <v-list-item-group>
                <template v-for="(item) in files">
                  <v-list-item :key="item.title">
                    <v-list-item-avatar>
                      <img :src="item.avatar">
                    </v-list-item-avatar>
                    <template>
                      <v-list-item-content>
                        <v-list-item-title v-html="item.title"></v-list-item-title>
                        <v-list-item-subtitle v-text="item.subtitle"></v-list-item-subtitle>
                      </v-list-item-content>
                      <v-list-item-action>
                        <v-btn v-text="item.actions" rounded color="cyan" small></v-btn>
                      </v-list-item-action>
                    </template>
                  </v-list-item>
                </template>
              </v-list-item-group>
            </v-list>
          </v-card>   
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default{
  name: 'Home',
  data() {
    return {
      search: '',
      desserts: [
        {
          glutenfree: false,
          name: '아지르',
          email: '99king@lol.com',
          rating: 0,
          status: 'Open',
        },
        {
          glutenfree: true,
          name: '녹턴',
          email: 'badream@lol.com',
          rating: 2,
          status: 'Open',
        },
        {
          glutenfree: false,
          name: '제라스',
          email: 'imfree@lol.com',
          rating: 2,
          status: 'Open',
        },
        {
          glutenfree: false,
          name: '킨드레드',
          email: 'loveyang@lol.com',
          rating: 5,
          status: 'Open',
        },
        {
          glutenfree: true,
          name: '레오나',
          email: 'ihatesun@lol.com',
          rating: 4,
          status: 'Open',
        },
        {
          glutenfree: false,
          name: '노틸러스',
          email: 'underthec@lol.com',
          rating: 2,
          status: 'Open',
        },
      ],
      headers: [
        {text: '', value: 'glutenfree'},
        {text: 'Name', align: 'start', sortable: false, value: 'name'},
        {text: 'Email', value: 'email'},
        {text: 'Rating', value: 'rating'},
        {text: 'Status', value: 'status', sortable: false},
        {text: 'Actions', value: 'action', sortable: false},
      ],
      files: [
        { 
          avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          actions: 'Closed',
          headline: '비비큐',
          subtitle: '황금 올리브',
          title: '<strong>갈리오 갈릴레이</strong>',
        },
        { 
          avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
          actions: 'Pending',
          headline: '네네 치킨',
          subtitle: '스노우윙 치즈',
          title: '<strong>괴체니체 나체</strong>',
        },
        { 
          avatar: 'https://cdn.vuetifyjs.com/images/lists/3.jpg',
          actions: 'Open',
          headline: '호식이 두마리 치킨',
          subtitle: '뭐시기 로제 치킨',
          title: '<strong>아이작 스턴</strong>',
        },
        { 
          avatar: 'https://cdn.vuetifyjs.com/images/lists/4.jpg',
          actions: 'Open',
          headline: '호식이 두마리 치킨',
          subtitle: '붕알치킨',
          title: '<strong>박혁 거세</strong>',
        },
      ],
    }
  }
}
</script>
<style scoped>
  .datatab{
    background: #23252D !important;
  }
</style>