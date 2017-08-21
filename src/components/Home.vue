<template>
  <div class="content">
    <Main></Main>
    <interstice></interstice>
    <References></References>
  </div>
</template>

<script>
import Main from './Main'
import Interstice from './Interstice'
import References from './References'

export default {
  name: 'hello',
  components: {
    Main,
    Interstice,
    References
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
div.content {
  position: absolute;
  top: 0;
}
  .rw-words{
    display: inline;
    text-indent: 10px;
    font-size: 0.8em;
  }
  .rw-words-1 span{
    position: absolute;
    opacity: 0;
    overflow: hidden;
    color: #6b969d;
    -webkit-animation: rotateWord 18s linear infinite 0s;
    -ms-animation: rotateWord 18s linear infinite 0s;
    animation: rotateWord 18s linear infinite 0s;
  }
  .rw-words-1 span:nth-child(2) { 
      -webkit-animation-delay: 3s; 
    -ms-animation-delay: 3s; 
    animation-delay: 3s; 
    color: #6b889d;
  }
  .rw-words-1 span:nth-child(3) { 
      -webkit-animation-delay: 6s; 
    -ms-animation-delay: 6s; 
    animation-delay: 6s; 
    color: #6b739d; 
  }
  .rw-words-1 span:nth-child(4) { 
      -webkit-animation-delay: 9s; 
    -ms-animation-delay: 9s; 
    animation-delay: 9s; 
    color: #7a6b9d;
  }
  .rw-words-1 span:nth-child(5) { 
      -webkit-animation-delay: 12s; 
    -ms-animation-delay: 12s; 
    animation-delay: 12s; 
    color: #8d6b9d;
  }
  .rw-words-1 span:nth-child(6) { 
      -webkit-animation-delay: 15s; 
    -ms-animation-delay: 15s; 
    animation-delay: 15s; 
    color: #9b6b9d;
  }
  @-webkit-keyframes rotateWord {
      0% { opacity: 0; }
      2% { opacity: 0; -webkit-transform: translateY(-30px); }
    5% { opacity: 1; -webkit-transform: translateY(0px);}
      17% { opacity: 1; -webkit-transform: translateY(0px); }
    20% { opacity: 0; -webkit-transform: translateY(30px); }
    80% { opacity: 0; }
      100% { opacity: 0; }
  }
  @-ms-keyframes rotateWord {
      0% { opacity: 0; }
      2% { opacity: 0; -ms-transform: translateY(-30px); }
    5% { opacity: 1; -ms-transform: translateY(0px);}
      17% { opacity: 1; -ms-transform: translateY(0px); }
    20% { opacity: 0; -ms-transform: translateY(30px); }
    80% { opacity: 0; }
      100% { opacity: 0; }
  }
  @keyframes rotateWord {
      0% { opacity: 0; }
      2% { opacity: 0; -webkit-transform: translateY(-30px); transform: translateY(-30px); }
    5% { opacity: 1; -webkit-transform: translateY(0px); transform: translateY(0px);}
      17% { opacity: 1; -webkit-transform: translateY(0px); transform: translateY(0px); }
    20% { opacity: 0; -webkit-transform: translateY(30px); transform: translateY(30px); }
    80% { opacity: 0; }
      100% { opacity: 0; }
  }
  body {
    font-family: 'Raleway';
    margin: 0;
  }
  .main-page a {
    color: white;
  }
  .main-page {
    background-color: #5CC1B0;
    color: white;
    height: 100vh;
    width: 100vw;
    position: absolute;
  }
  .logo {
    float: right;
    margin-right: 6vw;
  }
  h1{
    position: absolute;
    top: 30vh;
    left: 40vw;
    font-size: 3em;
    font-weight: 200;
  }
  .aboutus-button {
    position: absolute;
    bottom: 10vh;
    right: 36vw;
/*    border-bottom: 1px solid white;
    border-top: 1px solid white;
    padding-bottom: 4px;
    padding-top: 4px;
*/  }

.catch-phrase h2 {
  font-weight: 300;
}
.catch-phrase {
    height: 40vh;
    overflow: hidden;
    width: 100vw;
    /* margin-left: 30vw; */
    margin-top: -6px;
    color: white;
    padding: 6vh 0vw;
    text-align: center;
    font-family: 'Roboto';
    background-color: #C4C4C4;
    padding-top: 106vh;
}
.portfolio .headline {
  margin: 0px;
  font-weight: 600;
}
.portfolio .text {
  margin: 0px;
  font-weight: 400;
}
.portfolio .last-text {
  font-weight: 300;
}
.portfolio h2 {
  color: #666;
  font-weight: 400;
  font-size: 1.8em;
}
.portfolio img.small {
  width: 20vw;
}
.portfolio img {
    width: 36vw;
    float: right;
    margin-left: 6vw;
}
.portfolio {
  height: 66vh; 
  width: 80vw;
  margin-left: 10vw;
  color: #666;
  font-family: 'Roboto';
  background-color: white;
  padding: 16px;
  margin-top: 14vh;
  border-bottom: 1px solid #EEE;
  overflow: hidden;
}

/* Common button styles */
.button {
  float: left;
  min-width: 150px;
  max-width: 250px;
  display: block;
  margin: 1em;
  padding: 1em 2em;
  border: none;
  background: none;
  color: inherit;
  vertical-align: middle;
  position: relative;
  z-index: 1;
  -webkit-backface-visibility: hidden;
  -moz-osx-font-smoothing: grayscale;
}
.button:focus {
  outline: none;
}
.button > span {
  vertical-align: middle;
}

.button--text-thin {
  font-weight: 300;
}
.button--round-s {
  border-radius: 5px;
}
/* Borders */
.button--border-thin {
  border: 1px solid;
}

/* Individual button styles */
/* Ujarak */
.button--ujarak {
  -webkit-transition: border-color 0.4s, color 0.4s;
  transition: border-color 0.4s, color 0.4s;
}
.button--ujarak::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #37474f;
  z-index: -1;
  opacity: 0;
  -webkit-transform: scale3d(0.7, 1, 1);
  transform: scale3d(0.7, 1, 1);
  -webkit-transition: -webkit-transform 0.4s, opacity 0.4s;
  transition: transform 0.4s, opacity 0.4s;
  -webkit-transition-timing-function: cubic-bezier(0.2, 1, 0.3, 1);
  transition-timing-function: cubic-bezier(0.2, 1, 0.3, 1);
}
.button--ujarak.button--round-s::before {
  border-radius: 2px;
}
.button--ujarak.button--inverted::before {
  background: #7986CB;
}
.button--ujarak,
.button--ujarak::before {
  -webkit-transition-timing-function: cubic-bezier(0.2, 1, 0.3, 1);
  transition-timing-function: cubic-bezier(0.2, 1, 0.3, 1);
}
.button--ujarak:hover {
  color: #fff;
  border-color: #37474f;
}
.button--ujarak.button--inverted:hover {
  color: #37474F;
  border-color: #fff;
}
.button--ujarak:hover::before {
  opacity: 1;
  -webkit-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
}
</style>
