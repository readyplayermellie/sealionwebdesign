<template>
    <SmallerHeaderSection :title="title" />
    <WebsiteSection />
    <PackageSection />
    <MoreTestimonials />
    <SecondFooter />
</template>

<script>
export default {
    data() {
        return {
            title: 'Jouw zakelijke website waar de passie vanaf spat'
        }
    }
}
</script>