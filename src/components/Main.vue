<template>
    <main>
        <Intro/>
        <Videochannel/>
        <Playlist
        :itemvideos='videoLinks'/>
        <Subscribe/>
        <Plans 
        :itemtrainings='training'/>
        <Articles
        :itemarticles='articleLinks'/>  
        <Buy/>
        <Sponsors
        :itemsponsors='sponsorLinks'/>
        <Dayworkout/>
    </main>
</template>

<script>
import Intro from './Intro';
import Videochannel from './Videochannel';
import Playlist from './Playlist';
import Subscribe from'./Subscribe';
import Plans from './Plans'
import Articles from './Articles';
import Buy from './Buy';
import Sponsors from './Sponsors';
import Dayworkout from './Dayworkout';



export default {
    name: 'Main',
    components: {
        Intro,
        Videochannel,
        Playlist,
        Subscribe,
        Plans,
        Articles,
        Buy,
        Sponsors,
        Dayworkout
    },
    props:['videoLinks', 'articleLinks', 'sponsorLinks', 'training']

}
</script>

<style>

</style>