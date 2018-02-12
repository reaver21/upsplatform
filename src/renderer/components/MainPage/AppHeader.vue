<template>
  <header>
    <div class="win-opt" id="optCloseWin" v-on:click="closeWindow">&#x2716</div>
    <div class="win-opt" id="optMaxWin" v-on:click="maxWindow">&#x1f5d6</div>
    <div class="win-opt" id="optMinWin" v-on:click="minWindow">&#x1f5d5</div>
  </header>
</template>

<script>
  var { remote } = require('electron')
  export default {
    methods: {
      closeWindow: function () {
        var win = remote.getCurrentWindow()
        win.close()
      },
      maxWindow: function () {
        var win = remote.getCurrentWindow()
        win.isMaximized() ? win.unmaximize() : win.maximize()
      },
      minWindow: function () {
        var win = remote.getCurrentWindow()
        win.minimize()
      }
    }
  }
</script>

<style>
  header {
    display: flex;
    flex-direction: row-reverse;
    justify-content: flex-start;
    -webkit-app-region: drag;
    background: rgba(0,0,0,0.8);
    min-height: 40px;
  }

  .win-opt {
    color: white;
    padding: 5px 12px;
    font-size: 20px;
    cursor: pointer;
    -webkit-app-region: no-drag;
  }

  #optMinWin:hover {
    background: ghostwhite;
    color: black;
  }

  #optMaxWin:hover {
    background: ghostwhite;
    color: black;
  }

  #optCloseWin:hover {
    background: red;
  }
</style>