<template>
    <div class="box_animation container" v-if="loading">
        <div class="loader_spin"></div>
    </div>
</template>

<script>
export default {
    name: 'LoaderSpin'
}
</script>

<style lang="scss" scoped>
    .box_animation {
        padding: 3.125rem;
        display: flex;
        justify-content: center;
        align-items: center;
        .loader_spin {
            border: 1.25rem solid var(--text_primary);
            border-top: 1.25rem solid var(--primary_bg_color); /* Blue */
            border-radius: 50%;
            width: 12.5rem;
            height: 12.5rem;
            animation: spin 2s linear infinite;
        }
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }

</style>