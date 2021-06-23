<template>
  <section class='d-flex ms-videochannel'>
        <div class="ms-container ms-container-left position-relative">
            <img src="../assets/img/service15-2x.jpg" alt="">
            <i class="fas fa-play p-5 position-absolute top-50 start-50 translate-middle"></i>
        </div>
        <div class="ms-container d-flex flex-column justify-content-center align-items-start ms-5">
            <h3 class="mx-5">Tune up your workouts</h3>
            <h2 class="mx-5 py-4 display-4">The best health &amp; fitness advice online</h2>
            <div class="d-flex align-items-center mx-5">
                <img src="../assets/img/unnamed.jpg" alt="Symbol" class="me-2">
                <div>
                    <span class="">Theme Fusion</span>
                    <div class="d-flex align-items-center ms-youtube">
                        <i class="fab fa-youtube px-2 py-1"> YouTube</i>
                        <span class="px-1">999+</span>
                    </div>
                </div>
            </div>
            <p class="mx-5 py-3">Arcu eu facilisi ut quisque placerat nun habitant. Magna semper mauris, venenantis, leo integer sit pellentesque.</p>
            <div class='d-flex align-items-center ms-btn-full px-5 py-3 mx-5'>
                <i class="fab fa-youtube me-3 "></i>
                <a href="#"> Visit my YouTube channel</a>
            </div>
        </div>

  </section>
</template>

<script>
export default {
    name: 'Videochannel'

}
</script>

<style scoped lang='scss'>
    @import '../style/mixins.scss';

    .ms-videochannel{
        width: 100%;
        height: 700px;
        .ms-container{
            width: calc(100% / 2);
        }

        .ms-container-left{
            margin-top: -60px;
            
            img{
                width: 100%;
                height: 100%;
                border-radius: 5px 5px 70px 0px;
                object-position: center;
                object-fit: cover;
            }

            .fa-play{
                @include play-button;
            }
        }

        h3 {
            color: #4154fe;
        }
        span{
            color: #78787a;
            font-size: 0.9rem
        }
        p{
            color: #78787a;
            font-size: 20px;
        }

        .ms-youtube {
            border: 1px solid #bcbcbc;
            .fa-youtube {
            background-color: #f04e4b;
            color: white;
            }
        }
        
        

        .ms-btn-full{
            background-color:#f04e4b;
            border-radius: 25px;
            color: white;
            transition: all 0.3s;
            &:hover {
                background-color: #4154fe;
            }

            a {
                color: white;
                text-decoration: none;
            }
        }
    }
    
</style>