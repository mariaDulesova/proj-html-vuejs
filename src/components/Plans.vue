<template>
    <section class='py-5'>
        <div class="d-flex justify-content-between ms-wrap px-5 my-5">
            <div v-for="(training, index) in itemtrainings" :key="index" class="ms-service-card text-center mx-4 my-5 p-5">
                <img :src="require(`../assets/img/${training.icon}.svg`)" :alt="`${training.title}`" class="my-5">
                <h3>{{ training.title }}</h3>
                <h4>{{ training.subTitle }}</h4>
                <p class="mt-5"> {{ training.description }}</p>
                <a class="my-5">{{ training.link }} <i class="fas fa-chevron-right mx-2"></i></a>
            </div>  
        </div>
    </section>
</template>

<script>
export default {
    name: 'Plans',
    props: ['itemtrainings']
}
</script>

<style scoped lang='scss'>
    @import '../style/mixins.scss';

    section {
        background-color: #060606;

        .ms-wrap {
            @include my-wrap;

            .ms-service-card{
                border: 4px solid #4154fe;
                border-radius: 10px;

                h3{
                    color: white;
                }
                h4{
                    color: yellow;
                }
                p{
                    color: #bcbcbc;
                    line-height: 25px;
                    font-size: 17px;
                }
                a{
                    display: block;
                    text-decoration: none;
                    color: white;
                }
            }
        }   
           
    }

</style>