
 <template>
    <v-app>
    <v-app-bar
      absolute
      color="#fcb69f"
      dark
      shrink-on-scroll
      src="./assets/books.jpeg"
      scroll-target="#scrolling-techniques-1"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(22,11,255,.5), rgba(199,94,255,.8)"
        ></v-img>
      </template>
      <v-menu top :offset-x="offset">
            <template v-slot:activator="{ on }">
              <v-btn
                dark
                icon
                v-on="on"
              >
                <v-app-bar-nav-icon></v-app-bar-nav-icon>
              </v-btn>
            </template>

            <v-list>
              <v-list-item
                v-for="(item, i) in items"
                :key="i"
                @click="hi"
              >
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
      <v-spacer></v-spacer>
      <v-toolbar-title class="display-2 font-weight-black">Book Store</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-shopping</v-icon>
      </v-btn>
    </v-app-bar>
    <v-content class="content">
      <mainOne/>
    </v-content>
    </v-app>

</template>

<script>
import mainOne from './components/HelloWorld.vue'

export default {
  name: 'App',

  components: {
    mainOne
  },

  data: () => ({
    items: [
      { title: 'Home' },
      { title: 'Action' },
      { title: 'Drama' },
      { title: 'Fiction' },
      { title: 'Adventure' },
      { title: 'Historical' },
      { title: 'Science Fiction' },
      { title: 'Nonfiction' },
      { title: 'Romance' },
      { title: 'Science' }
    ]//
  })
}
</script>
