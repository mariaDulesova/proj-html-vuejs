<template>
    <main>
        <Intro/>
        <Videochannel/>
        <Playlist
        :itemvideos='videoLinks'/>
        <Articles
        :itemarticles='articleLinks'/>
    </main>
</template>

<script>
import Intro from './Intro';
import Videochannel from './Videochannel';
import Playlist from './Playlist';
import Articles from './Articles';


export default {
    name: 'Main',
    components: {
        Intro,
        Videochannel,
        Playlist,
        Articles
    },
    props:['videoLinks', 'articleLinks']

}
</script>

<style>

</style>