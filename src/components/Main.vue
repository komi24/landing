<template>
  <section class="main-page">
    <h1>We make it happen.<br>
    <div class="rw-words rw-words-1">
      <span>MVP - Prototype</span>
      <span>Progressive Web App</span>
      <span>Task automation</span>
      <span>Web application</span>
      <span>Task force Optimization</span>
      <span>Web application</span>
    </div>
    </h1>
    <div class="aboutus-button">
      <a href="#about"><button class="button button--ujarak button--border-thin button--round-s button--text-thin">About us</button></a>
    </div>
    <div style="height:100vh; overflow: hidden;">
          <div class="chat-window">
            <div class="chat-messages">
              <ol class="chat-messages-list" style="transform: matrix(1, 0, 0, 1, 0, 0);">
                <li class="chat-message chat-message-friend">
                  <div class="chat-message-bubble">
                    {{msgHello}}
                  </div>
                </li>
                </ol>
            </div>
            <div class="chat-input-bar">
              <div class="chat-info-container">

              </div>
              <div class="chat-effect-container" style="filter: none;">
                <div class="chat-effect-bar"></div>
              </div>
              <div class="chat-input-wrapper">
                <button class="chat-input-tool">
                  <i class="icon icon-camera"></i>
                </button>
                <div class="chat-input" contenteditable=""></div>
                <button class="chat-send">
                  <i class="fa fa-paper-plane" style="transform: translate3d(0px, 0px, 0px);"></i>
                </button>
              </div>
            </div>
          </div>    
    </div>
    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="800">
      <defs>
        <filter id="goo">
          <feGaussianBlur in="SourceGraphic" stdDeviation="10" result="blur"></feGaussianBlur>
          <feColorMatrix in="blur" mode="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 19 -9" result="goo"></feColorMatrix>
          <feComposite in="SourceGraphic" in2="goo"></feComposite>
        </filter>
      </defs>
    </svg>
  </section>
</template>

<script>
// var msgHello = window.location.search ? 'Hello, ' + window.atob(window.location.search.substring(1)) + '!' : 'Hello !'
export default {
  name: 'hello',
  data () {
    return {
      msgFollow: 'Tu souhaites réaliser un nouveau projet ?'
    }
  },
  computed: {
    msgHello: function () {
      console.log(window.location.search.substring(1))
      return window.location.search ? 'Hello, ' + window.atob(window.location.search.substring(1)) + '!' : 'Hello !'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.chat-window button:focus {
  -webkit-tap-highlight-color: rgba(255,255,255,0);
  -webkit-tap-highlight-color: transparent;
  outline: none;
}

.chat-window {
  width: 24vw;
  height: 70vh;
  margin: 4em 2em;
  overflow: hidden;
  border: 0px solid #36383a;
  border-width: 50px 15px;
  color: #474c57;
  border-radius: 20px;
  font-family: 'Avenir Next', 'Helvetica Neue', Helvetica, Arial, sans-serif;
}

@media screen and (max-width:380px) {
  .chat-window {
    border: none;
    border-radius: 0px;
  }
}

.chat-window a {
  color: #eab1c6;
}

.chat-window a:hover,
.chat-window a:focus {
  color: #C7668A;
}

.chat-messages {
  height: 60vh;
  /*height: 460px;*/
  overflow-x: hidden;
  overflow-y: auto;
  width: 100%;
  position: relative;
  border-radius: 2px 2px 0 0;
  background: #BEE4F9;
}

.chat-messages-list {
  list-style-type: none;
  padding: 0;
  margin: 0;
  width: 100%;
  padding: 15px 25px 60px;
}

.chat-message {
  position: relative;
  font-size: 0;
  margin-bottom: 10px;
  max-width: 19vw;
}

.chat-message-effect {
  position: absolute;
}

.chat-message-bubble {
  display: inline-block;
  font-size: 14px;
  max-width: 350px;
  background: #fff;
  padding: 8px 14px;
  border-radius: 18px;
  min-width: 0;
}

.chat-message-self.chat-message-merge-start .chat-message-bubble {
  border-bottom-right-radius: 0;
}

.chat-message-self.chat-message-merge-middle .chat-message-bubble {
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}

.chat-message-self.chat-message-merge-end .chat-message-bubble {
  border-top-right-radius: 0;
}

.chat-message-self {
  text-align: right;
}

.chat-message-self .chat-message-bubble,
.chat-message-effect .chat-message-bubble { 
  background: #32a8e6;
  color: #fff;
  text-align: left;
}

.chat-input-bar {
  position: relative;
  background:#32A8E6;
}

.chat-input-wrapper {
  position: relative;
  z-index: 2;
  /*background: #32A8E6;*/
  padding: 0.5em 0;
  border-radius: 0 0 2px 2px;
  color: #fff;
  height: 10vh;
}

.chat-input-wrapper,
.chat-send {
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-flex-wrap: wrap;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  -webkit-justify-content: center;
  justify-content: center;
  font-size: 16px;
}

.chat-input-tool {
  background: transparent;
  border: none;
  padding: 0 0.75em;
  color: inherit;
}

.chat-input {
  outline: none;
  resize: none;
  overflow: hidden;
  min-height: 38px;
  -webkit-flex: 1;
  flex: 1;
  font-size: 14px;
  padding: 10px 0 7px;
  cursor: text;
}

.chat-input:empty::before {
  content: "Write something...";
  color: #2B8EC2;
}

.chat-input:focus::before {
  content: "";
}

.chat-send {
  background: transparent;
  border: none;
  position: relative;
  overflow: hidden;
  padding: 0 0.75em;
  color: inherit;
  -webkit-transition: color 0.6s;
  transition: color 0.6s;
}

.chat-input:empty + .chat-send {
  color: #2B8EC2;
}

.chat-send>i {
  position: relative;
}

.chat-effect-container {
  position: absolute;
  top: -100px;
  width: 100%;
}

.chat-effect-bar {
  background: #32a8e6;
  position: absolute;
  top: 100px;
  width: 100%;
  height: 40px;
  -webkit-transform: rotateY(0);
  transform: rotateY(0);
}

.chat-effect-dots {
  position: absolute;
}

.chat-effect-dot {
  background: #32a8e6;
  position: absolute;
  width: 15px;
  height: 15px;
  border-radius: 100%;
}

.chat-info-container {
  position: absolute;
  top: -20px;
  font-size: 12px;
  color: #2B8EC2;
}

.chat-info-typing {
  position: absolute;
  left: 80px;
  white-space: nowrap;
}

</style>
