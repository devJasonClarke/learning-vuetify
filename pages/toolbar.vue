<template>
  <div>
 
    <v-btn elevation="2" @click="change">{{ text }}</v-btn>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "Please click me"
    };
  },
  methods: {
    change() {
      this.text = "thank you!";
    }
  }
};
</script>

<style lang="scss" scoped></style>
