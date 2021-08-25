<template>
  <div id="app">
    {{ info }}
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      info: null,
    };
  },
  mounted() {
    axios
      .get("api.coin.z.com/public/v1/ticker")
      .then((response) => (this.info = response));
  },
};
</script>
