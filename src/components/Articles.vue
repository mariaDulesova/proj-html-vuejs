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
                </div>
                <h5 class="text-center">{{ itemvideo.title }}</h5>
                <a href="#" class="text-center"> {{ itemvideo.subTitle }}</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Articles',
    props: ['itemvideos']

}
</script>

<style scoped lang="scss">
    .ms-wrap {
        width: 70%;
        margin: 0 auto;
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

       
    }
    
    

</style>