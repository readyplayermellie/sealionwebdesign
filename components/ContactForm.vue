<template>
    <form>
        <div v-for="(item, index) in contactItems" :key="index" class="mb-4">
            <label :for="item.id" class="w-full">{{ item.label }}</label>
            <textarea v-if="item.multiline" :id="item.id" class="w-full p-2 rounded-lg" rows="6"></textarea>
            <input v-else :type="item.type" :id="item.id" class="w-full p-2 rounded-lg">
        </div>
        <button class="btn btn-primary">Verstuur</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            contactItems: [
                {
                    label: 'Naam',
                    id: 'name',
                    type: 'text'
                },
                {
                    label: 'E-mailadres',
                    id: 'email',
                    type: 'text'
                },
                {
                    label: 'Bericht',
                    id: 'message',
                    type: 'text',
                    multiline: true
                }
            ]
        }
    }
}
</script>