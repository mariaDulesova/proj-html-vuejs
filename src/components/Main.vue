<template>
    <main>
        <Intro/>
        <Videochannel/>
        <Playlist
        :itemvideos='videoLinks'/>
        <Subscribe/>
        <Articles
        :itemarticles='articleLinks'/>  
        <Buy/>
        <Sponsors
        :itemsponsors='sponsorLinks'/>
    </main>
</template>

<script>
import Intro from './Intro';
import Videochannel from './Videochannel';
import Playlist from './Playlist';
import Subscribe from'./Subscribe';
import Articles from './Articles';
import Buy from './Buy';
import Sponsors from './Sponsors';


export default {
    name: 'Main',
    components: {
        Intro,
        Videochannel,
        Playlist,
        Subscribe,
        Articles,
        Buy,
        Sponsors
    },
    props:['videoLinks', 'articleLinks', 'sponsorLinks']

}
</script>

<style>

</style>