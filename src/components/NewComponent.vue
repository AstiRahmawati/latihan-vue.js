<template>
    <div>
        <Header text="Ini Adalah Header">
            <template #footer>
                <p>Ini Adalah Slot Dari Footer</p>
            </template>
        </Header>
        <MyComponent nama="asti" umur="10"></MyComponent>
        <LatihanComponent name="asti" age="20"></LatihanComponent>
        <Latihan2Component></Latihan2Component>
        <WatchersComponent nama="asti" umur="20"></WatchersComponent>
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
    </div>
</template>

<script setup>
import LatihanEventComponent from './LatihanEventComponent.vue';
import MyComponent from './MyComponent.vue';
import LatihanComponent from './LatihanComponent.vue';
import Latihan2Component from './Latihan2Component.vue';
import WatchersComponent from './WatchersComponent.vue';

// event
import {ref} from 'vue';
const nama = ref('John');
const umur = ref(25);

const onGreeted = () => {
    console.log('Kamu udah disapa, bro !')
};
</script>

<style>
</style>