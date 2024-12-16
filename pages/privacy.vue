<template>
    <SmallerHeaderSection :title="title" />
    <section>
        <p>{{ content }}</p>
    </section>
    <SecondFooter />
</template>

<script>
export default {
    data() {
        return {
            title: 'Privacyverklaring',
            content: 'In de maak en komt snel online!'
        }
    }
}
</script>