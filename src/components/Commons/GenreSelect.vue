<template>
<div class="row justify-content-center">
    <select class="custom_select col-5 p-2 mb-4">
        <option selected>Choose your genre</option>
        <option value="">1</option>
        <option value="">2</option>
        <option value="">3</option>
    </select>

</div>
</template>

<script>
export default {
    name: 'GenreSelect'

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