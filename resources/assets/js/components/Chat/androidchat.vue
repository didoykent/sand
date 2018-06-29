<template>


<v-app>

  <v-container grid-list-md text-xs-center>
      <v-layout row wrap>

          <v-flex xs12 >

   <v-subheader text-md-center>Active Users</v-subheader>

<v-list class="overflow-hidden py-0"  style="background-color:transparent;">
  <v-layout row align-content-center class="horiz-scroll">





    <v-flex
                     v-for="media in mediaList"
                     :key="media.id"
                     px-1
                     pb-2
                   >
                     <div class="pos-relative">

                       <img :src="media.src"  >
                       <div class  = "dot">
                            <span class="statusColor" style="  height: 15px;
                              width: 15px;
                              background-color: #81C784;
                              border-radius: 50%;
                                z-index: 1;

                          transform: translate(20px, -18px);

                              display: inline-block;" ></span>
                          </div>
                         <p style="transform: translateY(-70%);">{{media.name}}</p>
                     </div>
                   </v-flex>










</v-layout>


</v-list>
</v-flex >



</v-layout row align-content-center >




<v-subheader text-md-center>Users<v-flex xs4 offset-xs7 offset-lg8> <v-text-field
         light


         placeholder="Search"
              >
      </v-text-field></v-flex></v-subheader>




  <v-flex class ="scrollable">
   <v-list two-line   style="background-color:transparent;">
          <template v-for="(item, index) in items">
            <v-subheader v-if="item.header" :key="item.header">{{ item.header }}</v-subheader>
            <v-divider v-else-if="item.divider" :inset="item.inset" :key="index"></v-divider>
            <v-list-tile v-else :key="item.title" avatar @click="">
              <v-list-tile-avatar>
                <img :src="item.avatar">

                <v-badge top  overlap :color = "'green'" ><span slot="badge"  style = "height: 10px; width: 1px;"></span></v-badge>

              </v-list-tile-avatar>
              <v-list-tile-content>
                <v-list-tile-title v-html="item.title"></v-list-tile-title>
                <v-list-tile-sub-title v-html="item.subtitle"></v-list-tile-sub-title>
              </v-list-tile-content>
              <v-list-tile-action top>

                  <v-list-tile-sub-title  class = "text-lg-right" v-html="">8:30am</v-list-tile-sub-title>
            </v-list-tile-action>
            </v-list-tile>
          </template>
        </v-list>
      </v-flex>

</v-container>
</v-app>

</template>


<script>


export default{


data(){
  return {

mediaList: [
     {id: 1, name: "Tin", src: "https://scontent.ficn2-1.fna.fbcdn.net/v/t1.0-9/22281788_1586405444714343_8401123696989260119_n.jpg?_nc_cat=0&_nc_eui2=AeF4P9OVX7I1Dc68sNQQqoqIK7qGahZ07Eg2gGKqcS_tMWC4wfTySUS8mF9NfRqXv_hG1u7UJ30xhAtLrxiL9GzQeQwyjSJ5_Yht5aoMHkwXig&oh=dd25b8e4e0cecc0c5a47355d400278dd&oe=5B9EAF04"},
{id: 2, name: "John", src: "https://placeimg.com/200/200/arch"},
{id: 3, name: "Sarah", src: "https://placeimg.com/200/200/nature"},
{id: 4, name: "Mae", src: "https://placeimg.com/200/200/people"},
{id: 5, name: "June", src: "https://placeimg.com/200/200/tech"},
{id: 6, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 7, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 8, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 9, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 10, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 11, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 12, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 13, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 14, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 15, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 16, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 17, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 18, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 19, name: "John", src: "https://placeimg.com/200/200/animals"},
{id: 20, name: "John", src: "https://placeimg.com/200/200/animals"}
],


items: [

         { avatar: 'https://placeimg.com/200/200/arch', title: 'Brunch this weekend?', subtitle: "<span class='text--primary'>Ali Connors</span> &mdash; I'll be in your neighborhood doing errands this weekend. Do you want to hang out?" },

         { avatar: 'https://placeimg.com/200/200/people', title: 'Summer BBQ <span class="grey--text text--lighten-1">4</span>', subtitle: "<span class='text--primary'>to Alex, Scott, Jennifer</span> &mdash; Wish I could come, but I'm out of town this weekend." },

         { avatar: 'https://placeimg.com/200/200/nature', title: 'Oui oui', subtitle: "<span class='text--primary'>Sandra Adams</span> &mdash; Do you have Paris recommendations? Have you ever been?" },

         { avatar: 'https://placeimg.com/200/200/tech', title: 'Brunch this weekend?', subtitle: "<span class='text--primary'>Ali Connors</span> &mdash; I'll be in your neighborhood doing errands this weekend. Do you want to hang out?" },

         { avatar: 'https://placeimg.com/200/200/animals', title: 'Summer BBQ <span class="grey--text text--lighten-1">4</span>', subtitle: "<span class='text--primary'>to Alex, Scott, Jennifer</span> &mdash; Wish I could come, but I'm out of town this weekend." },

         { avatar: 'https://placeimg.com/200/200/animals', title: 'Oui oui', subtitle: "<span class='text--primary'>Sandra Adams</span> &mdash; Do you have Paris recommendations? Have you ever been?" },

         { avatar: 'https://placeimg.com/200/200/animals', title: 'Brunch this weekend?', subtitle: "<span class='text--primary'>Ali Connors</span> &mdash; I'll be in your neighborhood doing errands this weekend. Do you want to hang out?" },

         { avatar: 'https://placeimg.com/200/200/animals', title: 'Summer BBQ <span class="grey--text text--lighten-1">4</span>', subtitle: "<span class='text--primary'>to Alex, Scott, Jennifer</span> &mdash; Wish I could come, but I'm out of town this weekend." },

         { avatar: 'https://placeimg.com/200/200/animals', title: 'Oui oui', subtitle: "<span class='text--primary'>Sandra Adams</span> &mdash; Do you have Paris recommendations? Have you ever been?" },


       ]
}
 }
}




</script>

<style>




body{

  position: fixed;
  overflow-y: hidden;
  top: 0; right: 0; bottom: 0; left: 0;
}

.overflow-hidden {
  overflow: hidden;

}
.horiz-scroll {
  overflow-y: hidden;
  overflow-x: auto;
  max-width: 55vh;

},


.vert-scroll{

  overflow-x: hidden;
  overflow-y: auto;

}


.scrollable{

  overflow-x: hidden;
  overflow-y: auto;
  max-height: 55vh;
}

::-webkit-scrollbar {
    display: none;
}


img {
display:block;

max-width:54px;
max-height: 54px;
border-radius: 50%;



}

.dot {

}

.statusColor{
background-color:transparent;

}

</style>
