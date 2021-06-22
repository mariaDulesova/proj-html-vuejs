<template>
    <div class="ms-jambotron pb-5">
        <div class="ms-wrap d-flex justify-content-between align-items-center">
            <div class="d-flex flex-column justify-content-center ms-container">
                <h3 >Join our mailing list today</h3>
                <h1 class='py-3 display-3'>Insider offers &amp; flash sales in your inbox every week.</h1>
                <img src="../assets/img/wave.png" alt="Wave" width='80'>
                <form class="row mt-5">
                    <div class="col-7">
                        <input type="email" class="form-control" id="email" placeholder="Insert your email...">
                    </div>
                    <div class="d-grid col-4 ms-4">
                        <button type="submit" class=" btn py-3 ms-btn-full">Subscribe</button>
                    </div>
                </form>
                <p class='py-4'>Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet, consectetur adipiscing elit sed porttitor lectus.</p>
            </div>
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'Subscribe'

}
</script>

<style scoped lang='scss'>
    @import '../style/mixins.scss';
    
    .ms-jambotron {
        height: 700px;
        background-image: linear-gradient(to right, #060606 40%, #00000000),url('../assets/img/banner1-2x.jpg');
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
            }
            p {
                color:#bcbcbc;
                font-size: 20px;
            }
            .ms-container {
                width: 70%;
            }

            .ms-btn-full{
                @include my-main-button;
            }

            input{
                height: 100%;
                border-radius: 30px;
            }
          
        }
    }

</style>