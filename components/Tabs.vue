<template>
    <div>
        <ul class="tabs">
            <li 
                v-for="(title, index) in tab_titles" 
                :key="index"
                :class="{active: title == selected_title}"
                @click="selected_title = title"
            >
                {{ title }}
            </li>
        </ul>
        <slot />
    </div>
</template>

<script setup>
    const slots = useSlots()
    let tab_titles = ref(slots.default().map(tab => tab.props.title))
    let selected_title = ref(tab_titles.value[0])

    provide('selected_title', selected_title)
</script>

<style lang="scss">
    .tabs {
        display: flex;
        align-items: center;
        border-bottom: 3px solid var(--primary);
        margin-bottom: 10px;

        li {
            background-color: var(--secondary);
            // background-color: rgba(0, 0, 0, .4);
            margin-right: 4px;
            padding: 4px 10px;
            display: block;
            cursor: pointer;
            color: white;
            font-weight: 400;
            user-select: none;
            border-radius: 6px 6px 0 0;

            &.active {
                background-color: var(--primary);
                color: #222;
            }
        }
    }
</style>