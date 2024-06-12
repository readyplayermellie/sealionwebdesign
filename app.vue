<template>
  <Header />
  <main>
    <Intro />
    <Services />
    <About />
    <Contact />
  </main>
  <Footer />
</template>

<script setup>
useHead({
    title: 'Sea Lion Web Design & Development',
    meta: [
      {
        name: 'description',
        content: 'Web Design and Development | Freelance web developer for beautiful websites and user-friendly web tooling' 
      },
      {
        name: 'viewport',
        content: 'width=device-width, initial-scale=1'
      },
      {
        name: 'charset',
        content: 'utf-8'
      }
    ],
    htmlAttrs: { lang: 'nl' },
  });
useSeoMeta({
  title: 'Sea Lion Web Design & Development',
  ogTitle: 'Sea Lion Web Design & Development',
  description: 'Web Design and Development | Freelance web developer for beautiful websites and user-friendly web tooling',
  ogDescription: 'Web Design and Development | Freelance web developer for beautiful websites and user-friendly web tooling',
  ogImage: 'assets/content/header.png',
  ogType: 'website',
  ogUrl: 'https://www.sealionwebdesign.com'
})
</script>