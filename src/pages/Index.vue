<template>
  <q-page class="flex flex-center">
    <div class="row column">
      <h2>Contador</h2>
      <h1 class="flex flex-center">{{ contador }}</h1>
      <div class="flex flex-center">
        <q-btn
          push
          color="white"
          class="q-mr-md"
          text-color="primary"
          label="-"
          @click="less"
        />
        <q-btn
          push
          color="white"
          class="q-mr-md"
          text-color="primary"
          label="zero"
          @click="zero"
        />
        <q-btn
          push
          color="white"
          class="q-mr-md"
          text-color="primary"
          label="+"
          @click="sum"
        />
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
  data() {
    return {
      contador: 0,
    };
  },
  methods: {
    sum() {
      this.contador += 1;
    },
    zero() {
      this.contador = 0;
    },
    less() {
      this.contador -= 1;
    },
  },
};
</script>
