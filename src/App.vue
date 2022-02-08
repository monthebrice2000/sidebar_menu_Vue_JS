<template>
  <div :class="'main ' + (open ? 'open' : '')">
    <div class="aside">
      <div class="aside_header">
        <div class="logo_title" v-on:click="open_close()">
          <span class="logo"><img src="../public/img/streaming.png"></span><span class="title">AIR FORCE</span>
        </div>
      </div>
      <div class="aside_main">
        <div class="link dashboard">
          <span class="logo"><img src="../public/img/speed-test.png"></span>
          <span class="title">DASHBOARD</span>
        </div>
        <div class="link message">
          <span class="logo"><img src="../public/img/chat.png"></span>
          <span class="title">MESSAGE</span>
        </div>
        <div class="link user">
          <span class="logo"><img src="../public/img/teamwork.png"></span>
          <span class="title">USERS</span>
        </div>
        <div class="link rewards">
          <span class="logo"><img src="../public/img/medal.png"></span>
          <span class="title">REWARDS</span>
        </div>
        <div class="link reports">
          <span class="logo"><img src="../public/img/report.png"></span>
          <span class="title">REPORTS</span>
        </div>
        <div class="link settings">
          <span class="logo"><img src="../public/img/settings.png"></span>
          <span class="title">SETTINGS</span>
        </div>
      </div>
      <div class="footer"></div>
    </div>
    <div class="articles">ARTICLES</div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: () => {
    return {
      open: false,
    }
  },
  watch: {
    handler: (old, newValue) => {
      console.log( newValue );
    }
  },
  methods: {
    open_close : function() {
      this.open = this.open ? false : ( window.screen.width > 361 ? false : true );
      console.log( this.open)
    }
  }
}

</script>

<style>

</style>
