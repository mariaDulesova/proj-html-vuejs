<template>
    <header>
        <Nav
            :items='menulinks'
        />
        <Jambotron/>
    </header>
</template>

<script>
import Nav from '../components/Nav';
import Jambotron from '../components/Jambotron';

export default {
    name:'Header',
    components: {
        Nav,
        Jambotron
    },
    props: ['menulinks'],



}
</script>

<style scoped lang='scss'>
    header{
        background-color: #060606;
    }
</style>