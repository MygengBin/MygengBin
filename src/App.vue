<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <div>
    <button @click="black">黑色</button>
    <button @click="white">白色</button>
    <button @click="auto">跟随系统</button>
  </div>
  <router-view/>
</template>
<script lang="ts">
import {defineComponent} from 'vue';
const {body} = document;
export default defineComponent({
  methods:{
    black(){
      !body.classList.contains('dark') && body.classList.add('dark');
      body.classList.contains('light') && body.classList.remove('light');
    },
    white(){
      !body.classList.contains('light') && body.classList.add('light');
      body.classList.contains('dark') && body.classList.remove('dark');
    },
    auto(){
      body.classList.contains('light') && body.classList.remove('light');
      body.classList.contains('dark') && body.classList.remove('dark');
    },
  }
});
</script>

<style lang="scss">
@media (prefers-color-scheme: dark) {
    body {
      background: rgb(53, 54, 58);
      color: rgba(238,238,238,1);
    }
    nav{
    a{
        color:white;
        &.router-link-exact-active {
          color: gray;
        }
      }
  }
}

@media (prefers-color-scheme: light) {
    body {
      background: rgb(255,255,255);
      color: rgba(51,51,51,1);
    }
    nav {
        a {
          
          color: #2c3e50;

          &.router-link-exact-active {
            color: #42b983;
          }    
        }
      }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body{
  &.dark{
    background: rgb(53, 54, 58);
    color: rgba(238,238,238,1);
    h1,h2,h3,h4,h5,h6,p{
      color:white;
    }
    nav{
      a{
        color:white;
        &.router-link-exact-active {
          color: gray;
        }
      }
    }
  }      
  &.light{
    background: rgb(255,255,255);
    color: rgba(51,51,51,1);
    nav {
      a {
        color: #2c3e50;

        &.router-link-exact-active {
          color: #42b983;
        }    
      }
    }
  }
  nav{
    padding: 30px;
    a{
      font-weight: bold;
    }
  }
}
</style>
