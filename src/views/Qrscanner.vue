<template>
  <div class="QR">
    <h1>Qr scanner check</h1>
    <VueQrReader
      v-on:code-scanned="codeScanned"
      stop-on-scanned="true"
      use-back-camera="true"
      draw-on-found="true"
      line-color="#00FF00"
      line-width="20"
      video-height="480"
      video-width="640"
      responsive="true"
    />
  </div>
</template>

<script>
import VueQrReader from "vue-qr-reader/dist/lib/vue-qr-reader.umd.js";

export default {
  components: {
    VueQrReader
  },
  data() {
    return {
      scanned: ""
    };
  },
  methods: {
    codeArrived(code) {
      this.scanned = event.detail[0];
    }
  }
};
</script>