<template>
    <SmallerHeaderSection :title="title" />
    <WebsiteSection />
    <PackageSection />
    <MoreTestimonials />
    <SecondFooter />
</template>

<script setup>
const title = ref('Jouw zakelijke website waar de passie vanaf spat');
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