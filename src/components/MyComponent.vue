<template>
    <div>
        <h3>Nama : {{ nama }}</h3>
        <h3>Umur : {{ umur }}</h3>
        <h3>Jenis Kelamin : {{ jk }}</h3>
        <h3>Alamat : {{ almt }}</h3>
    </div>
</template>

<script>
export default {
    props:['nama','umur'],
    data() {
        return{
            jk: 'Perempuan',
            almt: 'Bandung'
        }
    }
}
</script>

<style>
h1{
    color: lavender;
}
p{
    color: pink;
}
</style>