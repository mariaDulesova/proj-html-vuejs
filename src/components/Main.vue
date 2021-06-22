<template>
    <main>
        <Intro/>
        <Videochannel/>
        <Playlist
        :itemvideos='videoLinks'/>
        <Subscribe/>
        <Articles
        :itemarticles='articleLinks'/>  
    </main>
</template>

<script>
import Intro from './Intro';
import Videochannel from './Videochannel';
import Playlist from './Playlist';
import Subscribe from'./Subscribe';
import Articles from './Articles';


export default {
    name: 'Main',
    components: {
        Intro,
        Videochannel,
        Playlist,
        Subscribe,
        Articles
    },
    props:['videoLinks', 'articleLinks']

}
</script>

<style>

</style>