<template>
    <div>
    <div v-if="this.$route.params.name">
        <h4>Customer</h4>
        [id: {{ this.$route.params.id }} - 
        name: {{ this.$route.params.name }}]
    </div>
    <div v-else>
        <br/>
        <p>Please click on a Customer...</p>
    </div>
    <button @click="test()">cuba</button>
    </div>

</template>

<script>
export default {
  name: "customer",
  data() {
    return {
      customers: null
    };
  },
    methods: {
      test(){
          this.customers = this.$route.params.name
          console.log(this.customers);
          
      }
  }
};
</script>