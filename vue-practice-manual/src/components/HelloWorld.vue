<template>
  <div>
    <div>{{ hi2 }}</div>
    <div v-if="hi">if test</div>
    <button
      type="button"
      v-on:click="shanghai"
      v-for="fruit in arr"
      v-bind:key="fruit"
    >
      {{ fruit }}
    </button>
    <Chat />
    <v-input 
    :messages="arr[3]" 
    append-icon="close" 
    prepend-icon="phone">
      Default Slot
    </v-input>
  </div>
</template>

<script>
import Chat from "basic-vue-chat";
export default {
  name: "HelloWorld",
  components: { Chat },
  data: () => {
    return {
      hi: "hello world",
      hi2: "nihao",
      arr: ["딸기", "당근", "수박", "참외", "메론"]
    };
  },

  methods: {
    shanghai: function() {
      window.alert("dimsum");
      this.hi = "";
    }
  }
};
</script>
