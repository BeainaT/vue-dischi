<template>
<div class="row justify-content-center">
    <select class="custom_select col-5 p-2 mb-4" v-model="selectedGenre" @click.prevent="$emit('search', selectedGenre)">
        <option value="all" selected>Choose your genre</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
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