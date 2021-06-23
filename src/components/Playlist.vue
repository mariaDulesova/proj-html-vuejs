<template>
    <section class='ms-wrap my-5 py-5'>
        <div class="d-flex justify-content-between align-items-center mx-3 my-5">
            <h4 >Featured playlists</h4>
            <span>View all videos<i class="fas fa-chevron-right mx-2"></i></span>
        </div>
        <div class='d-flex justify-content-between ms-container '>
            <div v-for="(itemvideo,index) in itemvideos" :key="index" class='mx-3 '>
                <div class="position-relative">
                    <img :src="require(`../assets/video/${itemvideo.url}.jpg`)" :alt="`${itemvideo.title}`" class="mb-4 ">
                    <i class="fas fa-play p-4 position-absolute top-50 start-50 translate-middle"></i>
                </div>
                <h5 class="text-center">{{ itemvideo.title }}</h5>
                <a href="#" class="text-center"> {{ itemvideo.subTitle }}</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Playlist',
    props: ['itemvideos']

}
</script>

<style scoped lang="scss">
    @import '../style/mixins.scss';

    .ms-wrap {
        @include my-wrap;
    }

    h4,h5{
        font-weight: 400;
    }

    .ms-container {
        img{
            width: 100%;
            border-radius: 10px 10px 70px 10px;
        }

        a{
            display: block;
            color:  #4154fe;
            text-decoration: none;
        }

        .fa-play{
            @include play-button;
            font-size: 0.7rem;
        }
    }
    
    

</style>
