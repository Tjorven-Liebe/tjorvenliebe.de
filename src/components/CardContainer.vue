<script setup>
import Card from "./Card.vue";

const frameworks = {
  spigot: {
    icon: 'spigot-icon',
    color: '#000'
  },
  paper: {
    icon: 'paper-icon',
    color: ''
  },
  bukkit: {
    icon: 'bukkit-icon',
    color: ''
  },
  rest: {
    icon: 'rest-icon',
    color: ''
  }
}

const others = {
  discord: {
    icon: 'fab fa-discord discord-icon',
    color: '#5B68F2'
  },
  data: {
    icon: 'fas fa-database',
    color: '#0f5c6f'
  },
  gradle: {
    icon: 'gradle-icon',
    color: ''
  },
  github: {
    icon: 'fab fa-github',
    color: '#F0F6FC'
  },
  linux: {
    icon: 'fab fa-linux',
    color: '#FFF'
  },
  jetbrains: {
    icon: 'jetbrains-icon'
  }
}

const webFrameworks = {
  node: {
    icon: 'node-icon',
    color: '#72A961'
  },
  yarn: {
    icon: 'fab fa-yarn',
    color: '#1E3050'
  },
  vue: {
    icon: 'fab fa-vuejs',
    color: '#41B883'
  },
  bootstrap: {
    icon: 'fab fa-bootstrap',
    color: '#8011F9'
  }
}

const languages = {
  kotlin: {
    icon: 'kotlin-icon'
  },
  java: {
    icon: 'java-icon',
    color: '#000'
  },
  css: {
    icon: 'fab fa-css3',
    color: '#89DDFF'
  },
  sass: {
    icon: 'fab fa-sass',
    color: '#C76494'
  },
  html: {
    icon: 'fab fa-html5 html-icon',
    color: '#E54C21'
  },
  js: {
    icon: 'fab fa-square-js',
    color: '#EFD81D'
  }
}
</script>

<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xl-3 col-lg-4 col-md-6">
        <ul class='circle-container con1'>
          <card v-for="stack in languages" v-bind:color="stack.color" v-bind:icon="stack.icon"
                v-bind:title="stack.title"></card>
        </ul>
      </div>
      <div class="col-xl-3 col-lg-4 col-md-6">
        <ul class='circle-container con2'>
          <card v-for="stack in frameworks" v-bind:color="stack.color" v-bind:icon="stack.icon"
                v-bind:title="stack.title"></card>
        </ul>
      </div>
      <div class="col-xl-3 col-lg-4 col-md-6 col-sm-12">
        <ul class="circle-container con3">
          <card v-for="stack in webFrameworks" v-bind:color="stack.color" v-bind:icon="stack.icon"
                v-bind:title="stack.title"></card>
        </ul>
      </div>
      <div class="col-xl-3 col-lg-12 col-md-6 col-sm-12">
        <ul class="circle-container con4">
          <card v-for="stack in others" v-bind:color="stack.color" v-bind:icon="stack.icon"
                v-bind:title="stack.title"></card>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>