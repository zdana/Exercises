<template>
  <div class="home">
    <Amap msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import Amap from "@/components/Amap/index.vue";

export default {
  name: "Index",
  components: {
    Amap,
  },
};
</script>
