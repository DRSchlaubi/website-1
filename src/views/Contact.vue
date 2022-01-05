<template>
  <div class="contact">
    <h1 class="subpage-title animate">Contact Me</h1>
    <div class="subtitle animate delay02">
      <p>
        Let's make something awesome!
      </p>
    </div>
    <div class="subpage-text animate delay04">
      <p>
        I love to collaborate with minecraft content creators and help to create the best content possible!
      </p>
    </div>
    <div class="subpage-text animate delay08">
      <p>
        If you think you have something awesome in mind feel free to contact me one of the platforms below.
      </p>
    </div>
    <div class="links animate delay1">
      <div class="link">
        <a class="on-hover text-color-secondary label-email copy-email"></a>
      </div>
      <div class="link">
        <a class="on-hover text-color-secondary link label-twitter" href="https://twitter.com/StckOverflw" target="_blank" rel="noopener noreferrer"></a>
      </div>
      <div class="link">
        <a class="on-hover text-color-secondary link label-discord" href="discord://-/users/816989010836717599" onclick="openDiscordFallback()"></a>
      </div>
    </div>
    <div class="subpage-text animate delay12">
      <p>
        You can also follow me on these other social media platforms:
      </p>
    </div>
    <div class="links animate delay14">
      <div class="link">
        <a class="on-hover text-color-secondary link" href="https://github.com/StckOverflw" target="_blank" rel="noopener noreferrer">GitHub</a>
      </div>
      <div class="link">
        <a class="on-hover text-color-secondary link" href="https://twitch.tv/StckOverflw" target="_blank" rel="noopener noreferrer">Twitch</a>
      </div>
    </div>
  </div>
</template>

<script>
import ClipboardJS from "clipboard";

function openDiscordFallback() {
  setTimeout(function() {
    window.location = "https://discordapp.com/users/816989010836717599";
  }, 200);
}

const clipboard = new ClipboardJS('.copy-email', {
  text: function () {
    return 'business@stckoverflw.net';
  }
});

clipboard.on('success', function(e) {
  console.log(e);
});
clipboard.on('error', function(e) {
  console.log(e);
});

import {Vue} from 'vue-class-component';

export default class Contact extends Vue { }
</script>

<style scoped>
  .label-email:before {
    content: "business@stckoverflw.net";
  }
  .label-email:hover:before {
    content: "Click to copy to clipboard";
  }
  .label-twitter:before {
    content: "Twitter";
  }
  .label-twitter:hover:before {
    content: "StckOverflw";
  }
  .label-discord:before {
    content: "Discord";
  }
  .label-discord:hover:before {
    content: "StckOverflw#2665";
  }
  .links {
    font-size: 1.5em;
    font-weight: bolder;
    margin-left: 10vmin;
  }
  .link {
    margin-bottom: 2vh;
  }
  .on-hover {
    transition: all .4s cubic-bezier(0.2, 0.6, 0.2, 1);
  }
  .on-hover:hover {
    margin-left: 20px;
    transition: all .4s cubic-bezier(0.2, 0.6, 0.2, 1);
  }
</style>
