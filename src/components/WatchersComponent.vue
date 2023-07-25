
<template>
    <h4>Nama Saya {{ nama }} </h4>
    <h4>Umur Saya {{ umur }}</h4>
    <button @click="cok">Sapa Dong</button>
</template>

<script>
export default {
  props: ['nama', 'umur'],
  data() {
    return {
      pesan: 'Halo, ' + this.nama + '!'
    };
  },
  methods: {
    cok() {
      alert('Halo, Bro!');
    }
  },
  computed: {
    pesanSelamat() {
      return 'Selamat datang, ' + this.nama + '!';
    }
  },
  watch: {
    umur(newUmur, oldUmur) {
      console.log('Umur berubah dari', oldUmur, 'menjadi', newUmur);
    }
  }
}
</script>