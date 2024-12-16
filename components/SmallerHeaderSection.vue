<template>
    <section id="website-header-section" class="smaller-section">
        <div class="small-content-container">
            <h2>{{ title }}</h2>
        </div>
        <img src="~/assets/content/dividers/waves/Blue-to-sand/sand-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    props: {
        title: String,
    }
}
</script>