<template>
     <section class='ms-wrap py-5'>
        <div class='d-flex justify-content-between ms-container my-5'>
            <div v-for="(itemsponsor,index) in itemsponsors" :key="index" class='mx-3 d-flex flex-column align-items-center'>
                <img :src="require(`../assets/img/${itemsponsor.label}.png`)" :alt="`${itemsponsor.name}`" >
                <img src="../assets/img/waveB.png" alt="White Wave" class="ms-wave my-4">
                <p class="px-3 text-center">{{ itemsponsor.description }}</p>
                <a href="#" class="my-3">{{ itemsponsor.link }}<i class="fas fa-chevron-right mx-2"></i></a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Sponsors',
    props: ['itemsponsors']

}
</script>

<style scoped lang='scss'>
    @import '../style/mixins.scss';

    .ms-wrap {
        @include my-wrap;

        .ms-wave{
            width: 50px;
        }

        img{
            width: 160px;
        }
        p{
            color:  #78787a;
            text-decoration: none;
            line-height: 30px;
        }
        a{
            text-decoration: none;
            color: #060606;
            transition: all 0.2s;
            &:hover{
                transform: scale(1.1);
                color: #4154fe;
            }

            i{
                font-size: 0.9rem;
            }
        } 
    }
</style>