<template>
     <section class='ms-wrap py-5'>
        <div class='d-flex justify-content-between ms-container my-5'>
            <div v-for="(itemsponsor,index) in itemsponsors" :key="index" class='mx-3 d-flex flex-column align-items-center'>
                <img :src="require(`../assets/img/${itemsponsor.label}.png`)" :alt="`${itemsponsor.name}`" class="mb-5">
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
    .ms-wrap {
        width: 70%;
        margin: 0 auto;

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

            i{
                font-size: 0.9rem;
            }
        }
        
    }
</style>