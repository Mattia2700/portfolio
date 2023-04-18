<template>
  <div></div>
</template>

<script>
import { saveAs } from 'file-saver';

export default {
  mounted() {
    fetch("./assets/CV - Mattia Franzin.pdf")
      .then((response) => response.blob())
      .then((blob) => {
        saveAs(blob, "CV - Mattia Franzin.pdf");
      });
  }
}
</script>

<style scoped>
/* your component styles */
</style>