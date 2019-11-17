
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

      <v-app-bar-nav-icon></v-app-bar-nav-icon>

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
    //
  })
}
</script>
