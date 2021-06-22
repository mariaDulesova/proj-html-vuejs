<template>
    <section class='ms-wrap my-5 py-5'>
        <div class="d-flex justify-content-between align-items-center mx-3 my-5">
            <h4>Latest Articles</h4>
            <span>Read all articles<i class="fas fa-chevron-right mx-2"></i></span>
        </div>
        <div class='d-flex justify-content-between ms-container '>
            <div v-for="(itemarticle,index) in itemarticles" :key="index" class='mx-3 '>
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
    .ms-wrap {
        width: 70%;
        margin: 0 auto;
    }
    h4{
        font-weight: 400;
    }

    .ms-container {
        img{
            width: 100%;
           
        }


        p{
            display: block;
            color:  #78787a;
            text-decoration: none;
        }

       
    }
    
    

</style>