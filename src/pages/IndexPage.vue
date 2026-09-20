<template>
  <main class="page">

    <section class="left">

      <nav>
        <div class="logo">●</div>

        <a
          v-for="menu in ['SERVICES','OFFICES','TEAM','PHILOSOPHY','SPACES']"
          :key="menu"
          href="#"
          :class="{ active: activeMenu === menu }"
          @click.prevent="activeMenu = menu"
        >
          {{ menu }}
        </a>
      </nav>

      <div class="profile">

        <div class="info">
          <small>OUR TEAM</small>
          <hr>
          <span>Sams Alif</span>
          <h2>Frontend<br>Developer</h2>
          <a class="explore" href="#">Explore</a>
        </div>

        <div class="art">

          <div class="big-circle"></div>

          <div class="small-circle"></div>

          <div class="dots"></div>

          <img
            src="/sams.png.jpeg"
            alt="Sams Alif"
          >

          <div class="arc"></div>

        </div>

      </div>
    </section>


    <section class="right">

      <button class="login">LOGIN</button>

      <div class="hero-text">
        <h1>
          Your legal advisers<br>
          for the problems<br>
          of this century
        </h1>

        <p>
          We offer solutions adapted to<br>
          today's needs
        </p>

        <button class="view">VIEW MORE</button>
      </div>

    </section>

  </main>
</template>


<script setup>
import { ref } from 'vue'

const activeMenu = ref('OFFICES')
</script>


<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

body{
  background:#fff;
  font-family:Georgia,serif;
}

.page{
  width:100%;
  min-height:100vh;
  display:grid;
  grid-template-columns:63% 37%;
}


/* LEFT */

.left{
  position:relative;
  overflow:hidden;
  background:#fff;
}

nav{
  height:90px;
  display:flex;
  align-items:center;
  gap:58px;
  padding:0 55px;
  font:700 13px Georgia,serif;
  letter-spacing:.5px;
}

nav a{
  color:#333;
  text-decoration:none;
}

nav a.active{
  color:#ff6267;
  border-top:2px solid #ff6267;
  padding-top:14px;
}

.logo{
  width:28px;
  height:20px;
  background:#ff6267;
  border-radius:0 0 20px 20px;
  color:white;
  text-align:center;
  margin-right:15px;
}


/* PROFILE */

.profile{
  position:relative;
  height:calc(100vh - 90px);
}

.info{
  position:absolute;
  z-index:10;
  left:45px;
  top:230px;
  width:180px;
}

.info small{
  font:700 12px Arial,sans-serif;
  letter-spacing:1.5px;
  color:#555;
}

.info hr{
  width:95px;
  margin:8px 0 20px;
  border:0;
  border-top:1px solid #555;
}

.info span{
  color:#333;
  font:900 24px Arial,sans-serif;
}

.info h2{
  margin-top:10px;
  font:normal 23px/1.25 Georgia,serif;
}

.explore{
  display:inline-block;
  margin-top:25px;
  color:#ff6267;
  text-decoration:none;
  border-bottom:1px solid #ff6267;
  padding-bottom:3px;
}


/* IMAGE AREA */

.art{
  position:absolute;
  width:650px;
  height:520px;
  left:170px;
  top:80px;
}

.big-circle{
  position:absolute;
  width:350px;
  height:350px;
  left:190px;
  top:80px;
  background:#ff6267;
  border-radius:50%;
}

.small-circle{
  position:absolute;
  width:65px;
  height:65px;
  left:30px;
  top:110px;
  background:#ff6267;
  border-radius:50%;
}

.dots{
  position:absolute;
  z-index:3;
  width:105px;
  height:105px;
  left:420px;
  top:165px;

  background-image:
    radial-gradient(#111 1.5px,transparent 1.5px);

  background-size:7px 7px;
}


/* MAIN PERSON */

.art img{
  position:absolute;
  z-index:4;

  /* size */
  width:430px;
  height:500px;

  /* position */
  left:120px;
  top:20px;

  /* important */
  object-fit:contain;
  object-position:center bottom;

  /* black & white like reference */
  filter:grayscale(100%);

  /* NO multiply */
  mix-blend-mode:normal;

  /* remove rectangular edges */
  background:transparent;

  /* person shape */
  clip-path:ellipse(47% 49% at 50% 52%);
}


/* ARC */

.arc{
  position:absolute;
  z-index:6;

  width:380px;
  height:380px;

  left:65px;
  top:105px;

  border:3px solid #ff6267;
  border-right-color:transparent;
  border-bottom-color:transparent;

  border-radius:50%;

  transform:rotate(-45deg);
}


/* RIGHT */

.right{
  position:relative;
  background:#ff6267;
  color:#fff;
}

.login{
  position:absolute;
  right:55px;
  top:27px;

  width:105px;
  height:42px;

  border:2px solid white;
  border-radius:0 0 18px 18px;

  background:transparent;
  color:white;

  font-weight:bold;
}

.hero-text{
  position:absolute;
  left:12%;
  top:27%;
}

.hero-text h1{
  font-size:38px;
  line-height:1.12;
  margin-bottom:25px;
}

.hero-text p{
  font:16px/1.5 Arial,sans-serif;
}

.view{
  margin-top:40px;

  width:125px;
  height:42px;

  border:0;
  border-radius:0 0 20px 0;

  background:white;
  color:#ff6267;

  font-weight:bold;
}


/* TABLET */

@media(max-width:1100px){

  nav{
    gap:30px;
    padding:0 30px;
  }

  .art{
    left:100px;
    transform:scale(.85);
    transform-origin:top left;
  }

}


/* MOBILE */

@media(max-width:700px){

  .page{
    grid-template-columns:1fr;
  }

  nav{
    gap:15px;
    padding:0 20px;
  }

  nav a{
    display:none;
  }

  .info{
    left:25px;
    top:180px;
  }

  .art{
    left:100px;
    top:80px;
    transform:scale(.7);
    transform-origin:top left;
  }

  .right{
    min-height:500px;
  }

  .hero-text h1{
    font-size:30px;
  }
}
</style>