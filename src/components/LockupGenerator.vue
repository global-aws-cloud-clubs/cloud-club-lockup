<template>
  <div>
    <h1>Let's Build a Cloud Club logo!</h1>
    <form @submit.prevent="onSubmit">
      <label>
        Your Club Name
        <input 
          v-model="input"
          type="text"
        >
      </label>

      <button type="submit">Download</button>
    </form>
  </div>
  <div id="logo">
    <img src="../assets/logo.png">
    <div class="club-name" v-text="input" id="output"></div>
  </div>
</template>

<script>
import { ref } from 'vue'
import * as htmlToImage from 'html-to-image';

export default {
  setup() {
    const input = ref('');

    const onSubmit = () => {
      
      var node = document.getElementById('logo');
      
  htmlToImage.toSvg(node)
  .then(function (dataUrl) {
    var link = document.createElement('a');
    link.download = 'my-cloud-cloud-logo.svg';
    link.href = dataUrl;
    link.click();
  });
        
    }

    return {
      input,
      onSubmit
    }
  }
}
</script>
