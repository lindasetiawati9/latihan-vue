<template>
    <div v-if="age > 18">
        <p>Selamat Datang {{ name }}</p>
    </div>
    <div v-else>
        <p>Maaf Kamu Belum Cukup Umur</p>
    </div>
    <button @click="greet">Sapa</button>
</template>
<script>
export default {
    props: ['name','age'],
    methods: {
        greet() {
            alert("Haloo " + this.name);
        }
    }
}
</script>