<template>
    <div class="ms-jambotron pb-5">
        <div class="ms-wrap d-flex justify-content-between align-items-center">
            <div class="d-flex flex-column justify-content-center">
                <h3 >Certified fitness professional</h3>
                <h1 class='py-3 display-3'>Take control of your health</h1>
                <img src="../assets/img/wave.png" alt="Wave" width='80'>
                <p class='py-4'>Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet.</p>
                <div class='d-flex'>
                    <div class='d-flex align-items-center ms-btn-full px-5 py-3'>
                        <i class="fab fa-youtube me-3"></i>
                        <a href="#"> Visit my YouTube channel</a>
                    </div>
                    <div class='d-flex align-items-center ms-btn-empty ms-4 px-5 py-3' >
                        <a href="#"> Buy Avada today</a>
                        <i class="fas fa-arrow-right ms-3"></i>
                    </div>
                </div>
            </div>
            <i class="fas fa-play p-5"></i>
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'Jambotron'

}
</script>

<style scoped lang='scss'>
    @import '../style/mixins.scss';

    .ms-jambotron {
        height: 800px;
        background-image: linear-gradient(to right, #060606 40%, #06060600),url('../assets/img/slider82x-scaled.jpg');
        background-position: right top;
        background-size: cover;
        background-repeat: no-repeat;

        .ms-wrap{
            @include my-wrap;
            height: 100%;

            h3{
                color: #f04e4b;
            }
            h1{
                color:white;
            }
            p {
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
            .ms-btn-empty {
                border: 3px solid #78787a;
                border-radius: 30px;
                transition: all 0.3s;
                &:hover{
                    background-color: white;
                    border-color: white;
                }
                &:hover a{
                    color: #78787a;
                }
                &:hover .fas{
                    color: #78787a;
                }

                a, .fas {
                    color: white;
                    text-decoration: none;
                }
            }

            .fa-play{
                @include play-button;
            }
        }
    }

</style>