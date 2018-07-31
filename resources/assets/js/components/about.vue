<template>
    <h1>{{message}}</h1>
</template>

<script>
    export default {
        name: "about",
        data() {
            return {
                message: ""
            }
        },
        created() {
            axios.post('/getabout').then(response => {
                console.log(response.data);
                this.message = response.data;
            })
        }
    }
</script>

<style scoped>

</style>