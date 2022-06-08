<template>
<div class="row justify-content-center">
    <select class="custom_select col-5 p-2 mb-4" v-model="selectedGenre" @click.prevent="$emit('search', selectedGenre)">
        <option value="all" selected>Choose your genre</option>
        <option value="Rock">1</option>
        <option value="Pop">2</option>
        <option value="Jazz">3</option>
        <option value="Metal">3</option>
    </select>
</div>
</template>

<script>
export default {
    name: 'MainSelect',
    data() {
        return {
            selectedGenre: '',
        }
    }

}
</script>

<style lang="scss" scoped>
    .custom_select {
        background-color: var(--main_bg_color);
        color: var(--text_secondary);
        // border-color: var(--primary_bg_color);
        &:focus {
            outline: none;
        }
    }

</style>