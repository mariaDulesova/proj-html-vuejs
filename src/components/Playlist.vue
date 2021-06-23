<template>
    <section class='ms-wrap my-5 py-5'>
        <div class="d-flex justify-content-between align-items-center mx-3 my-5">
            <h4 >Featured playlists</h4>
            <a href="#">View all videos<i class="fas fa-chevron-right mx-2"></i></a>
        </div>
        <div class='d-flex justify-content-between ms-container '>
            <div v-for="(itemvideo,index) in itemvideos" :key="index" class='mx-3 text-center'>
                <div class="position-relative">
                    <img :src="require(`../assets/video/${itemvideo.url}.jpg`)" :alt="`${itemvideo.title}`" class="mb-4 ">
                    <i class="fas fa-play p-4 position-absolute top-50 start-50 translate-middle"></i>
                </div>
                <h5>{{ itemvideo.title }}</h5>
                <span href="#"> {{ itemvideo.subTitle }}</span>
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
    a{
        text-decoration: none;
        color: #060606;
        transition: all 0.2s;
        &:hover{
            transform: scale(1.1);
            color: #4154fe;
        }
    }

    .ms-container {
        img{
            width: 100%;
            border-radius: 10px 10px 70px 10px;
        }

        span{
            display: block;
            color:  #4154fe;
        }

        .fa-play{
            @include play-button;
            font-size: 0.7rem;
        }
    }
    
    

</style>
