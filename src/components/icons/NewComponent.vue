<template>
    <headers a="Header"></headers><br>
    <fieldset><MyComponent nama="Linda" umur="17"></MyComponent></fieldset>
    <center><latihanComponent name="Linda Setiawati" age="20"></latihanComponent></center>
    <latihanDuaComponent></latihanDuaComponent><hr>
    <WatchersComponent nama="Ucup" umur="16"></WatchersComponent>
    <h2>Event Component</h2>
        <latihan-event-component :nama="nama" :umur="umur" @greeted="onGreeted">
            <template #footer>
                <div>
                    <p>Ini Adalah Footer Latihan Event</p>
                </div>
            </template>
            <template #header>
                <div>
                    <p>Ini Adalah Header latihan Event</p>
                </div>
            </template>
        </latihan-event-component>
</template>

<script setup>
import LatihanEventComponent from './EventComponent.vue';
import MyComponent from '../MyComponent.vue';
import headers from './headers.vue';
import latihanComponent from '../latihanComponent.vue';
import latihanDuaComponent from '../latihanDuaComponent.vue';
import WatchersComponent from '../WatchersComponent.vue';

// event
import { ref } from 'vue';
const nama = ref('John');
const umur = ref(25);

const onGreeted = () => {
    console.log('Kamu udah disapa, bro!');
};
</script>

<!-- kegunaan setup: tidak butuh logic js (export default)
Non setup: perlu logic js (export default) -->
