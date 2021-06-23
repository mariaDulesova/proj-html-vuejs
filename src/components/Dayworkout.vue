<template>
    <section class="d-flex flex-column justify-content-center align-items-center">
        <i class="fas fa-play"></i>
        <h2 class="text-center display-4 my-4">Crossfit workout of the day</h2>
        <h3 class='text-center display-6'>November 15th, 2019</h3>
        <a href="#" class='my-4'> View all videos <i class="fas fa-long-arrow-alt-right ms-1"></i></a>   
    </section>
</template>

<script>
export default {
    name: 'Dayworkout'

}
</script>

<style scoped lang='scss'>
    @import '../style/mixins.scss';

    section{
        height: 705px;
        background-image: linear-gradient(to bottom right, #0213918f, #66002994), url('../assets/img/banner14-2x.jpg');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;

        .fa-play{
            @include play-button;
            padding: 35px;
        }

        h2{
            color: white;
        }
        h3 {
            color: yellow;
        }
        a {
            color: white;
            text-decoration: none;
            font-size: 20px;
        }
    }
</style>