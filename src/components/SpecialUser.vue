<template>
    <div>
        <h1 ref="user_tag"></h1>
    </div>
</template>

<script>
    export default {

        methods: {
            handle_user_clicked(username) {
                this.$refs[`user_tag`][`innerText`] = username;
            }
        },
        mounted () {
            this.$root.$on(`user_clicked`, this.handle_user_clicked);
        },
    }
</script>

<style scoped>

</style>