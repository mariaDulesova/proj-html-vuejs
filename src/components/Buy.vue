<template>
  <section class="d-flex flex-column justify-content-center align-items-center">
        <q class="text-center my-5">I've failed over and over again in my life. And that is why I succeed</q>
        <img src="../assets/img/wave.png" alt="Wave" width='80'>
        <p class='text-center py-4'>Arcu auctor gravida nisl, congue sit nisi tincidunt eget proin. In lacinia lacus donec sed massa in ipsum eros, tristique. Gravida suspendisse etiam in iaculis</p>
        <div class='d-flex align-items-center ms-btn-full ms-4 px-5 py-3' >
            <a href="#"> Buy Avada today</a>
            <i class="fas fa-arrow-right ms-3"></i>
        </div>
  </section>
</template>

<script>
export default {
    name: 'Buy'

}
</script>

<style scoped lang='scss'>
    @import '../style/mixins.scss';

    section{
        height: 705px;
        background-image: linear-gradient(to top, #060606 , #06060600), url('../assets/img/banner2-2x.jpg');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;

        q{
            width: 50%;
            font-size: 3rem;
            color: white;
        }
        p {
            width: 50%;
            color:#bcbcbc;
            font-size: 20px;
        }
        .ms-btn-full{
            @include my-main-button;

            a {
                color: white;
                text-decoration: none;
            }
        }
            
    }

    

</style>