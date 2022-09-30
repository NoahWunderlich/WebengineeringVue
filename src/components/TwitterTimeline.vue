<template>
      <div class="bottomBar-blog-socialmedia">
        <a class="twitter-timeline" href="https://twitter.com/HochschuleFL?s=20&t=XxklDWYORdSbWAun4lUCsA"> </a>
      </div>
  </template>
  
  <script>
  export default {

    name: 'TwitterTimeline',
    data(){
      return{
        
      }
    },
    mounted() {
      const twitterScript = document.createElement('script');
      twitterScript.setAttribute('src', 'https://platform.twitter.com/widgets.js');
      twitterScript.setAttribute('async', 'async');
      document.head.appendChild(twitterScript);
    },
  }
  </script>
  
  <style>
    .twitter-timeline {
      width: 100% !important;
      height: 100px !important;
  }
  
  </style>
  