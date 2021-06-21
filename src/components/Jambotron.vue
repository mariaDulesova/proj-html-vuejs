<template>
    <div class="ms-jambotron">
        <div class="ms-wrap d-flex justify-content-between align-items-center">
            <div class="d-flex flex-column justify-content-center">
                <h3 class='py-3'>Certified fitness professional</h3>
                <h1>Take control of your health</h1>
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
    .ms-jambotron {
        height: 670px;
        background-image: linear-gradient(to right, #060606 40%, #06060600),url('../assets/img/slider82x-scaled.jpg');
        background-position: right top;
        background-size: cover;
        background-repeat: no-repeat;

        .ms-wrap{
            width: 70%;
            height: 100%;
            margin: 0 auto;

            h3{
                color: #f04e4b;
            }
            h1{
                color:white;
                font-size: 4rem;
                letter-spacing: 4px;
                font-weight: 500;
            }
            p {
                color:#bcbcbc;
                font-size: 20px;
            }

            .ms-btn-full{
                background-color: #4154fe;
                border-radius: 25px;
                color: white;
                transition: all 0.3s;
                &:hover {
                    background-color: #f04e4b;
                }

                a {
                    color: white;
                    text-decoration: none;
                }
            }
            .ms-btn-empty {
                border: 2px solid #78787a;
                border-radius: 25px;
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
                display:block;
                background-color: white;
                border-radius: 50%;
                color: #4154fe;
            }
        }
    }

</style>