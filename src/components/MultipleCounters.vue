<template>
 <v-container >
    <v-layout row class="justify-center mt-md-14" align-center>
        <v-flex md6>
        
            <v-row justify="center" align="center" class="ma-5 text-h6 font-weight-bold">{{title}}</v-row>
            
            <click-counter v-for="item in nbcounters" :key="item" v-on:incrementotalcount="incrementotalcount()"> </click-counter>
           
            <v-row justify="center" align="center" class="mt-5">
                  <v-btn  depressed color="primary" v-on:click="addcounter()" >ADD A COUNTER</v-btn>
            </v-row>

            <v-row justify="center" align="center" class="mt-5">
                 then sum of all the counters is equal to <v-chip color="gray ma-2" text-color="black">  {{ totalcount}}</v-chip> !
                  </v-row>
              
            <v-row  justify="center" align="center" v-if="nbcounter > 1">(i am rendred if there is more than one counter...) </v-row>    
            
        </v-flex>
      </v-layout>
 </v-container>
</template>

<script>
import ClickCounter from './ClickCounter.vue'

export default {
  components: { ClickCounter },
  data : function () {
                return {
                      title : "Multiple counters component",
                      nbcounters : 1,
                      totalcount : 0
                      }
                      },
  methods:{
              addcounter:function(){
                  this.nbcounters++;
              },
              incrementotalcount : function(){
                  this.totalcount++;
              }
      }

}
</script>

<style>

</style>