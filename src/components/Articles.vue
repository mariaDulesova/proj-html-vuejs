<template>
    <section class='ms-wrap my-5 py-5'>
        <div class="d-flex justify-content-between align-items-center mx-3 my-5">
            <h4>Latest Articles</h4>
            <a href="#">Read all articles<i class="fas fa-chevron-right mx-2"></i></a>
        </div>
        <div class='d-flex justify-content-between ms-container '>
            <div v-for="(itemarticle,index) in itemarticles" :key="index" class='mx-3 ms-img-container'>
                <div class="position-relative">
                    <img :src="require(`../assets/img/${itemarticle.url}.jpg`)" :alt="`${itemarticle.title}`" class="mb-4 ">
                </div>
                <h4 class="px-3">{{ itemarticle.title }}</h4>
                <p class="px-3"> {{ itemarticle.post }}</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Articles',
    props: ['itemarticles']

}
</script>

<style scoped lang="scss">
    @import '../style/mixins.scss';

    .ms-wrap {
        @include my-wrap;

        h4{
        font-weight: 400;
        }
        a{
            color: #060606;
            text-decoration: none;
            transition: all 0.2s;

            &:hover{
                transform: scale(1.1);
                color: #4154fe;
            }
        }
        .ms-container {

            .ms-img-container{
                transition: all 0.2s;
                &:hover{
                 transform: scale(1.1);
                }

                img{
                    width: 100%;
                }
                p{
                    color:  #78787a;
                    text-decoration: none;
                }

            }
            
        }
    }
</style>