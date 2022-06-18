<template>
    <div class="tab" v-show="props.title == selected_title">
        <slot />
    </div>
</template>

<script setup>
    let props = defineProps(['title'])
    let selected_title = inject('selected_title')
</script>