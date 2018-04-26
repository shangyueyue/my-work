<template>
  <div class="parent">
    <span class="center">this is nested rules</span>
    <div class="son">{{msg}}</div>
    <div @click="handleClick">
    {{ age }}
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      msg: 'shangyy',
      age: 18,
    };
  },
  methods: {
    handleClick() {
      this.res = 186;
      console.log("router",this.$router);
      console.log("route",this.$route);
      console.log('this.document')
    },
  },
  computed: {
    res: {
      get() {
        return 1;
      },
      set(t) {
        this.age = t;
      },

    },
  },
  watch: {
    age() {
    },
  },
};
</script>
<style scoped lang="less">
@import "../../common/less/mixins";
   .parent{
     .flex();
   }
  .son{
     width:100px;
     height:20px;
  }


</style>
