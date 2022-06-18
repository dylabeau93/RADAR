<template>
    <div class="navbar">
        <div class="logo">
            <NuxtLink to="/">
                <h2>RADAR</h2>
            </NuxtLink>
        </div>

    </div>
</template>
<script setup>


</script>

<style lang="scss">
    .navbar {
        border-bottom: 1px solid #222;
        padding: 12px 15px;

        .logo {
            h2 {
                color: var(--secondary);
            }
        }
    }
</style>