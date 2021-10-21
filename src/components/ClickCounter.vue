<template>
    <v-row justify="center" align="center">
        <v-btn class="mr-10" elevation="2" v-on:click="increment()" >CLICK HERE TO INCREMENT</v-btn>
        <v-chip v-if="count < 10" class="ma-2 pl-md-4" color="black" text-color="white">{{ count }}</v-chip>
        <v-chip v-if="count >= 10" class="ma-2 pl-md-4" color="red" text-color="white">{{ count }}</v-chip>
    </v-row>
</template>

<script>

export default {
  data: function () {
    return {count: 0,
    totalcount : 0}
  },
  methods: {
  increment: function () {
    this.count++;
    this.$emit('incrementotalcount');
  }}
}
</script>

<style>

</style>