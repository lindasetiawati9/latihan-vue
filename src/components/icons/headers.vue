<template>
    <div>
        <!-- Props -->
        <h2>Halo ini adalah {{ a }}</h2>
    </div>
</template>

<script>
export default {
    name: "headers",
    props:['a'],
    data() {
        return {
            message: "Ini Pesan Dari Komponen"
        }
    },
    methods: {
        greet() {
            console.log("Haloo");
        }
    }
}
</script>
<style>
h2{
    text-align: center;
    color: black;
    background-color: lightcoral;
}
</style>