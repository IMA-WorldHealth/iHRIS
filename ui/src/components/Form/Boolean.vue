<template>
  <v-checkbox
    :label="label"
    :value="checked"
    v-model="boolean"
    :hint="hint"
  ></v-checkbox>
</template>

<script>
export default {
  created() {
    this.boolean = this.checked;
  },
  data() {
    return {
      boolean: false
    };
  },
  methods: {
    getInput() {
      return this["boolean"];
    }
  },
  props: ["checked", "label", "hint"]
};
</script>
