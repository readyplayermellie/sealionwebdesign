<template>
    <SmallerHeaderSection :title="title"/>
    <AboutSection />
    <SecondFooter />
</template>

<script setup>
const title = ref('Wat is Sea Lion Web Design eigenlijk?');
useHead({
  script: [ 
    { 
      src: 'https://www.googletagmanager.com/gtag/js?id=G-KG0F9FTQNX'
    },
    {
      innerHTML: `window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-KG0F9FTQNX');`
    }
  ]
})
</script>