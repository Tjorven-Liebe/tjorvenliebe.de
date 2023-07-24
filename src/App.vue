<script setup>
import CardContainer from "./components/CardContainer.vue";
import Card from "./components/Card.vue";
import {frameworks, languages, others, webFrameworks} from "./stackinfo";

window.onload = () => {
  const brand = document.getElementById("brand");
  const brand1 = document.getElementById("brand1");
  const brand2 = document.getElementById("brand2");
  const brand3 = document.getElementById("brand3");

  const brand1icon = document.getElementById("brand1-icon");
  const brand2icon = document.getElementById("brand2-icon");
  const brand3icon = document.getElementById("brand3-icon");

  const container1 = document.getElementById("con1")
  const container2 = document.getElementById("con2")
  const container3 = document.getElementById("con3")
  const container4 = document.getElementById("con4")

  const skills = document.getElementById("skills")
  const about = document.getElementById("about")
  const contact = document.getElementById("contact")
  const footer = document.getElementById("footer")

  if (scrollY >= 1400) {
    brand.style.top = 50 + ((-scrollY + 1325) / 8) + 'vh'
  } else {
    brand.style.top = 40 + 'vh'
  }

  window.onscroll = () => {
    const s = 50 + (-scrollY / 8)
    const s1 = 50 + ((-scrollY + 340) / 8)
    const s2 = 50 + ((-scrollY + 680) / 8)

    if (scrollY <= 350) {
      brand1.style.top = s + 'vh'
      brand1icon.style.opacity = '0'
    } else if (scrollY >= 600) {
      brand1.style.top = (s + 30.5) + 'vh'
      brand1icon.style.opacity = '0'
    } else {
      brand1icon.style.opacity = '1'
      brand1.style.top = '6vh'
    }
    if (scrollY <= 700) {
      brand2.style.top = s1 + 'vh'
      brand2icon.style.opacity = '0'
    } else if (scrollY >= 950) {
      brand2.style.top = (s1 + 30.5) + 'vh'
      brand2icon.style.opacity = '0'
    } else {
      brand2.style.top = '6vh'
      brand2icon.style.opacity = '1'
    }
    if (scrollY <= 1050) {
      brand3.style.top = s2 + 'vh'
      brand3icon.style.opacity = '0'
    } else {
      brand3.style.top = '6vh'
      brand3icon.style.opacity = '1'
    }
    if (scrollY >= 1400) {
      brand.style.top = 50 + ((-scrollY + 1325) / 8) + 'vh'
    } else {
      brand.style.top = 40 + 'vh'
    }

    console.log(scrollY)

    if (scrollY < 2100) {
      skills.style.opacity = '0'
      container1.style.display = 'none'
      container2.style.display = 'none'
      container3.style.display = 'none'
      container4.style.display = 'none'
    }

    if (scrollY > 2100 && scrollY <= 2200) {
      skills.style.opacity = '1'
      container1.style.display = 'block'
      container2.style.display = 'none'
      container3.style.display = 'none'
      container4.style.display = 'none'
    }
    if (scrollY > 2500 && scrollY <= 3000) {
      container1.style.display = 'none'
      container2.style.display = 'block'
      container3.style.display = 'none'
      container4.style.display = 'none'
    }
    if (scrollY > 3000 && scrollY <= 3500) {
      container1.style.display = 'none'
      container2.style.display = 'none'
      container3.style.display = 'block'
      container4.style.display = 'none'
    }
    if (scrollY > 3500 && scrollY <= 4000) {
      container1.style.display = 'none'
      container2.style.display = 'none'
      container3.style.display = 'none'
      container4.style.display = 'block'
      skills.style.opacity = '1'
      skills.style.display = 'block'
      about.style.opacity = '0'
      about.style.display = 'none'
      console.log('toggle')
    }
    if (scrollY > 4000 && scrollY <= 4500) {
      skills.style.opacity = '0'
      skills.style.display = 'none'
      contact.style.opacity = '0'
      contact.style.display = 'none'
      about.style.opacity = '1'
      about.style.display = 'block'
    }
    if (scrollY > 4500 && scrollY <= 5000) {
      skills.style.opacity = '0'
      skills.style.display = 'none'
      about.style.opacity = '0'
      about.style.display = 'none'
      contact.style.opacity = '1'
      contact.style.display = 'block'
      footer.style.opacity = '0'
      footer.style.display = 'none'
    }
    if (scrollY > 5000) {
      contact.style.opacity = '0'
      contact.style.display = 'none'
      footer.style.opacity = '1'
      footer.style.display = 'block'
    }
  }
}

</script>

<template>
  <div id="top" class="top"></div>
  <div id="brand" class="brand" style="overflow: hidden">
    <div class="innerbox"
         style="position:absolute; border: 2px solid var(--color-border); padding: 25px 20px; border-radius: 20px; width: 80px; height: 100%; top: 50%; transform: translateY(-50%); right: 0">
      <i class="fas fa-computer-mouse fa-2x"></i><br/>
      <i class="fas fa-chevron-down fa-2x"></i>
    </div>
    <h1 class="">Tjorven Liebe..</h1>
    <i id="brand1-icon" class="fas fa-code fa-2x"
       style="opacity: 0; transition: 1s; position: fixed; top: 50%; transform: translateY(-50%); left: 0; width: 80px; height: 100%; padding: 40px 10px; border: 2px solid var(--color-border); border-radius: 20px"></i>
    <h2 id="brand1" style="opacity: 1; position: fixed; top: 20vh; left: 50%; transform: translateX(-50%); width: 100%">
      a software
      developer</h2>
    <i id="brand2-icon" class="fas fa-earth fa-2x"
       style="opacity: 0; transition: 1s; position: fixed; top: 50%; transform: translateY(-50%); left: 0; width: 80px; height: 100%; padding: 40px 10px; border: 2px solid var(--color-border); border-radius: 20px"></i>
    <h2 id="brand2"
        style="opacity: 1; position: fixed; top: 100vh; left: 50%; transform: translateX(-50%); width: 100%">a web
      developer</h2>
    <i id="brand3-icon" class="fas fa-user-friends fa-2x"
       style="opacity: 0; transition: 1s; position: fixed; top: 50%; transform: translateY(-50%); left: 0; width: 80px; height: 100%; padding: 40px 10px; border: 2px solid var(--color-border); border-radius: 20px"></i>
    <h2 id="brand3"
        style="opacity: 1; position: fixed; top: 200vh; left: 50%; transform: translateX(-50%); width: 100%">and a
      friend</h2>
  </div>
  <section id="skills" style="position: fixed;">
    <hr>
    <h1 class="text-center">My Skills</h1>
    <hr>
    <div class="stacktree">
      <div id="con1" class="showcase-content">
        <ul class='circle-container con1'>
          <card v-for="stack in languages" v-bind:color="stack.color" v-bind:icon="stack.icon"
                v-bind:title="stack.title"></card>
        </ul>
      </div>
      <div id="con2" class="showcase-content">
        <ul class='circle-container con2'>
          <card v-for="stack in frameworks" v-bind:color="stack.color" v-bind:icon="stack.icon"
                v-bind:title="stack.title"></card>
        </ul>
      </div>
      <div id="con3" class="showcase-content">
        <ul class="circle-container con3">
          <card v-for="stack in webFrameworks" v-bind:color="stack.color" v-bind:icon="stack.icon"
                v-bind:title="stack.title"></card>
        </ul>
      </div>
      <div id="con4" class="showcase-content">
        <ul class="circle-container con4">
          <card v-for="stack in others" v-bind:color="stack.color" v-bind:icon="stack.icon"
                v-bind:title="stack.title"></card>
        </ul>
      </div>
    </div>
    <hr style="position: absolute; bottom: 0; width: 100%; height: 3px">
  </section>
  <section id="about">
    <hr>
    <h1 class="text-center">About me</h1>
    <hr>
    <div>
      <h3>Hi, I'm Tjorven!</h3>
      <h5>What do I have to say about myself?</h5>
      <p>Well..</p>
      <ul>
        <li>I'm a German developer <i class="fas fa-beer"></i></li>
        <li>I'm a software developer <i class="fas fa-code"></i> since 2018</li>
        <li>I started coding with minecraft plugin</li>
        <li>and a web-developer <i class="fas fa-earth"></i> since 2020</li>
        <li>My favourite languages are Java <i class="fab fa-java"></i> and CSS <i class="fab fa-css3"></i> </li>
      </ul>
    </div>
    <hr style="position: absolute; bottom: 0; width: 100%; height: 3px">
  </section>
  <section id="contact">
    <hr>
    <h1 class="text-center">Contact me</h1>
    <hr>
    <div>
      <h3>So you wanna contact me?</h3>
      <h4>Here are my information</h4>
    </div>
    <hr style="position: absolute; bottom: 0; width: 100%; height: 3px">
  </section>
  <section id="footer">
    <hr>
    <h1 class="text-center">Legal Terms</h1>
    <hr>
    <div>
      <h3>As a German citizen, I surely have to be bureaucratic!</h3>
      <a href="impressum">Imprint</a><br/>
      <a href="data-protection.html">Data Protection Regulation</a>
    </div>
    <hr style="position: absolute; bottom: 0; width: 100%; height: 3px">
  </section>
</template>
<style lang="scss" scoped>

#skills, #about, #contact, #footer {
  position: fixed;
  left: 0;
  top: 0;
  width: 100vw;
  height: 100vh;
  transition: 1s;
  opacity: 0;
  > div {

    h1 {
      text-align: center;
      font-size: 40pt;
    }
    h2 {
      text-align: center;
      font-size: 35pt;
    }
    h3 {
      text-align: center;
      font-size: 30pt;
    }
    h4 {
      text-align: center;
      font-size: 25pt;
    }
    h5{
      text-align: center;
      font-size: 20pt;
    }
    * {
      font-size: 18pt;
    }
    width: 30%;
    margin: 2% auto
  }
}

.showcase-content {
  position: fixed;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

//.hidden {
//  transition: 1s;
//  opacity: 0;
//  display: none;
//}

</style>
