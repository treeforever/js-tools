<template>
  <div id='canvas-page'>
    <span>Canvas: {{ user }} is here</span>
    <canvas id='canvas'></canvas>
    <span>
      <a href="https://twitter.com/intent/tweet?button_hashtag=beautifulcanvas&ref_src=twsrc%5Etfw" class="twitter-hashtag-button" data-show-count="false">Tweet</a>
    </span>
  </div>
</template>

<style>
#dog {
  height: 10em;
}
#canvas {
  height: 100%;
  width: 100%;
  background: yellow;
}
</style>

<script>
export default {
  data() {
    return {
      user: 'Mengqi',
    };
  },

  methods: {
    fetchTwitterScript() {
      fetch('https://platform.twitter.com/widgets.js');
    },
  },
};
</script>
