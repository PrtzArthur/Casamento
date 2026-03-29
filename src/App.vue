<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import flores from '@/assets/flores.png'
import primeiro from '@/assets/primeiro.png'
import segundo from '@/assets/segundo.png'
import terceiro from '@/assets/terceiro.png'
import ultimo from '@/assets/ultimo.png'
import registry from '@/assets/registry.png'
import ultimaimagem from '@/assets/ultimaimagem.png'
import envio from '@/assets/envio.png'
import stars from '@/assets/stars.png'
</script>

<template>
  <header class="header">
    <div class="left">
      <span class="logo">J&amp;J</span>
      <span class="date">June 23rd, 2025</span>
    </div>

    <nav class="nav">
      <a href="#">HOME</a>
      <a href="#">OUR HISTORY</a>
      <a href="#">DETAILS</a>
      <a href="#">RSVP</a>
    </nav>
  </header>

  <main>
    <section class="section1">
      <div class="div1">
        <h1>JENNY & JASON</h1>
      </div>
    </section>
    <section
      class="section2"
      :style="{
        backgroundImage: `linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url(${flores})`,
      }"
    >
      <p>
        With love and gratitude, we invite you to <br />
        share in the joy of our wedding day.
      </p>
      <p>
        Saturday, September 20, 2025<br />
        The Golden Elm Manor,<br />
        St. Augustine, New York
      </p>
    </section>
    <section class="section3">
      <div class="card" :style="{ backgroundImage: `url(${primeiro})` }">
        <span>OUR HISTORY</span>
      </div>

      <div class="card" :style="{ backgroundImage: `url(${segundo})` }">
        <span>THE DETAILS</span>
      </div>

      <div class="card" :style="{ backgroundImage: `url(${terceiro})` }">
        <span>RSVP</span>
      </div>

      <div class="card" :style="{ backgroundImage: `url(${ultimo})` }">
        <span>REGISTRY</span>
      </div>
    </section>
    <section
      class="section4"
      :style="{
        backgroundImage: `url(${registry})`,
      }"
    >
      <h2>REGISTRY</h2>
      <p>
        Your presence is the most cherished gift. Should you wish to contribute, we’ve created a
        honeymoon registry to help us embark on a memorable adventure to the Amalfi Coast
      </p>
      <button>GO TO REGISTRY</button>
    </section>
    <section class="section5">
      <div class="box">
        <h2>RATE MY MARRIAGE</h2>
        <p>Got some free time? I have an idea! Rate my wedding!!</p>
        <div class="avaliacao">
          <img class="stars" :src="stars" alt="stars" />
          <img class="envio" :src="envio" alt="envio" />
        </div>
      </div>
    </section>
  </main>
  <footer>
    <h1>J&J</h1>
    <p>SATURDAY</p>
    <p>SEPTEMBER 20, 2025</p>
  </footer>
</template>

<style scoped>
/* ============================= FOOTER  ============================= */
footer {
  background-color: #C4B6AB;
  color: black;
  text-align: center;
  padding: 30px 20px;
  font-family: 'Georgia', serif;
}
h1{
  font-family: 'Instrument Serif', serif;
  font-size: 100px;
  margin-bottom: 10px;
}
footer p {
  font-size: 50px;
  font-family: 'Instrument Serif', serif;
  line-height: 40px;
}
/* ============================= SECTION5  ============================= */
.avaliacao {
  display: flex;
  flex-direction: column;
  align-items: center;
}
p {
  font-size: 50px;
  margin: 20px 0;
}
h2 {
  font-family: 'Instrument Serif', serif;
  font-size: 60px;
  margin-bottom: 20px;
}
.section5 {
  background-color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 80px 0;
}
.box {
  height: 800px;
  width: 1300px;

  background-image: url('@/assets/ultimaimagem.png');
  background-size: cover;
  background-position: center;

  padding: 150px 20px;
  text-align: center;
  color: white;

  position: relative;
}
.box::before {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.4);
}
.box h2,
.box p,
.box img {
  position: relative;
  z-index: 1;
}
/* ============================= SECTION4  ============================= */
.section4 {
  position: relative;
  background-size: cover;
  background-position: center;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  text-align: center;
  padding: 200px 20px;
  color: white;
}
.section4::before {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.4);
}
.section4 h2,
.section4 p,
.section4 button {
  position: relative;
  z-index: 1;
}
.section4 h2 {
  font-family: 'Adamina', serif;
  font-size: 60px;
  margin-bottom: 20px;
}

.section4 p {
  max-width: 600px;
  font-size: 25px;
  line-height: 1.6;
  margin-bottom: 30px;
}
.section4 button {
  background: transparent;
  border: 1px solid white;
  color: white;
  padding: 12px 30px;
  font-size: 14px;
  letter-spacing: 2px;
  cursor: pointer;
  font-family: 'Adamina', serif;
}

.section4 button:hover {
  background: white;
  color: black;
  transition: 0.3s;
}
/* ============================= SECTION3  ============================= */
.section3 {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;

  align-items: center;
  justify-items: center;
  padding: 50px;
  background-color: #eee;
}

.card {
  height: 700px;
  width: 600px;
  border-radius: 15px;

  background-size: cover;
  background-position: center;

  display: flex;
  align-items: center;
  justify-content: center;

  position: relative;
  overflow: hidden;
}

.card::before {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.3);
  border-radius: 15px;
}

.card span {
  position: relative;
  color: white;
  font-size: 20px;
  font-family: 'Georgia', serif;

  border-bottom: 1px solid white;
  padding-bottom: 5px;
}
/* ============================= SECTION2 ============================= */
.section2 {
  font-size: 40px;
  color: white;
  font-family: 'Abyssinica SIL', sans-serif;

  background-size: cover;
  background-position: center;
  background-image: url('@/assets/flores.png');

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 250px 20px;
}
.section2 p {
  margin: 10px 0;
  text-align: center;
}
/* ============================= DIV1/SECTION1 ============================= */

.div1 h1 {
  font-family: 'Instrument Serif', serif;
  font-size: 200px;
  text-align: center;
  margin-top: 20px;
  color: black;
}
.div1 {
  background-color: white;
  padding: 100px 20px;
}
/* ============================= HEADER ============================= */
.header {
  background-color: #4b4543;
  color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 40px;
  padding-bottom: 30px;
  font-family: 'Georgia', serif;
}

.left {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-left: 30px;
  font-family: 'Instrument Serif', serif;
}

.logo {
  font-size: 30px;
  margin-right: 20px;
}

.date {
  font-size: 25px;
  opacity: 0.8;
}

.nav a {
  color: #fff;
  text-decoration: none;
  margin-left: 50px;
  margin-right: 50px;
  font-size: 20px;
  position: relative;
}

.nav a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -5px;
  width: 100%;
  height: 1px;
  background-color: #fff;
  opacity: 0.5;
}
/* ============================= MOBILE ============================= */
@media (max-width: 768px) {

  /*=== HEADER ===*/
  .header {
    flex-direction: column;
    gap: 10px;
    text-align: center;
  }

  .nav {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
  }

  .nav a {
    margin: 0;
    font-size: 14px;
  }

  /*=== SECTION1 ===*/
  .div1 h1 {
    font-size: 60px;
  }

  /*=== SECTION2 ===*/
  .section2 {
    font-size: 20px;
    padding: 100px 20px;
  }

  /*=== SECTION3 ===*/
  .section3 {
    grid-template-columns: 1fr; /* vira coluna */
    padding: 20px;
  }

  .card {
    width: 100%;
    height: 400px;
  }

  /*=== SECTION4 ===*/
  .section4 {
    padding: 100px 20px;
  }

  .section4 h2 {
    font-size: 35px;
  }

  .section4 p {
    font-size: 18px;
  }

  /*=== SECTION5 ===*/
  .box {
    width: 90%;
    height: auto;
    padding: 100px 20px;
  }

  .section5 h2 {
    font-size: 35px;
  }

  .section5 p {
    font-size: 18px;
  }

  .stars {
    width: 180px;
  }

  .envio {
    width: 60px;
  }

  /*=== FOOTER ===*/
  footer h1 {
    font-size: 50px;
  }

  footer p {
    font-size: 20px;
    line-height: normal;
  }

}
</style>