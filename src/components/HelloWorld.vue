<template>
    <div id="app">
  <!-- <div class="hello" v-show="!show">
      <img src= "../assets/Lamborghini.png" />
      {{msg}}
  </div>
  <button @click="tache">点一下试试</button> -->

    <div class="Grid">
    <div class="Grid-cell">...</div>
    <div class="Grid-cell">...</div>
    <div class="Grid-cell">...</div>
    <div class="Grid-cell">...</div>
    <div class="Grid-cell">...</div>
    </div>
      <hr/>
<div class="Grid">
  <div class="Grid-cell u-1of4">...</div>
  <div class="Grid-cell">...</div>
  <div class="Grid-cell u-1of3">...</div>
</div>
    <hr/>
<div class="HolyGrail">
  <header>...</header>
  <div class="HolyGrail-body">
    <main class="HolyGrail-content">...</main>
    <nav class="HolyGrail-nav">...</nav>
    <aside class="HolyGrail-ads">...</aside>
  </div>
  <footer>..123.</footer>
</div>
<hr/>
<div class="InputAddOn">
  <span class="InputAddOn-item">China</span>
  <input class="InputAddOn-field">
  <button class="InputAddOn-item">√</button>
    <span class="InputAddOn-item">China</span>
  <input class="InputAddOn-field">
  <button class="InputAddOn-item">√</button>
</div>
  <hr/>
<div class="Media">
  <img class="Media-figure" src="../assets/logo.png" alt="英雄不问出处">
  <p class="Media-body">hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
        hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
  </p>
    <img class="Media-figure" src="../assets/logo.png" alt="英雄不问出处">
  <p class="Media-body">hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
    hello,naoiwisiuaw,qwdbuqbsabwk,qwbdusbajw,qwduyvsjavwd,aksdbywja
  </p>
</div>
<button @click="screenfull()">全屏</button>
    </div>
</template>

<script>
import screenfull from 'screenfull'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
      return {
        show:false,
        aurl:"../assets/Lamborghini.png"
      }
  },
  methods: {
    tache() {
      console.log(this)
    this.show = !this.show;
      //  let addre= ["../assets/Lamborghini.png","../assets/horse.png"]
      //  if(this.show == true){
      //    this.aurl = addre[0]
      //  }else{
      //    this.aurl  = addre[1]
      //  }
  },
   screenfull() {
      if (!screenfull.enabled) {
        this.$message({
          message: 'Your browser does not work',
          type: 'warning'
        })
        return false
      }
      screenfull.toggle()
      this.isFullscreen = true
    },
    /**
     * 是否全屏并按键ESC键的方法
     */
    checkFull() {
      var isFull = document.fullscreenEnabled || window.fullScreen || document.webkitIsFullScreen || document.msFullscreenEnabled
      // to fix : false || undefined == undefined
      if (isFull === undefined) {
          isFull = false
      }
      return isFull
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.Grid {
  display: flex;
}

.Grid-cell {
  flex: 1;
  border: 2px solid black;
}

.Grid {
  display: flex;
}

/* .Grid-cell {
  flex: 1;
} */

/* .Grid-cell.u-full {
  flex: 0 0 100%;
} */

/* .Grid-cell.u-1of2 {
  flex: 0 0 50%;
} */

/* .Grid-cell.u-1of3 {
  flex: 0 0 80%;
} */

.Grid-cell.u-1of4 {
  flex:0 60% 0;
}
.HolyGrail {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
}

header,
footer {
  flex: 1;
  background-color: limegreen;
  max-height: 5em;
}

.HolyGrail-body {
  display: flex;
  flex: 1;
}

.HolyGrail-content {
  flex: 1;
  background-color: magenta;
}

.HolyGrail-nav, .HolyGrail-ads {
  /* 两个边栏的宽度设为12em */
  flex: 0 0 12em;
  background-color: mediumturquoise;
}

.HolyGrail-nav {
  /* 导航放到最左边 */
  order: -1;
  background-color: navy;
}
@media (max-width: 768px) {
  .HolyGrail-body {
    flex-direction: column;
    flex: 1;
  }
  .HolyGrail-nav,
  .HolyGrail-ads,
  .HolyGrail-content {
    flex: auto;
  }
}
.InputAddOn {
  display: flex;
}

.InputAddOn-field {
  flex: 1;
}

.Media {
  display: flex;
  align-items: flex-start;
}

.Media-figure {
  margin-right: 1em;
}

.Media-body {
  flex: 1;
}

</style>
