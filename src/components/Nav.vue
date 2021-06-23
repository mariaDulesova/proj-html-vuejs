<template>
    <nav class='d-flex justify-content-between align-items-center ms-wrap py-4'>
        <img src="../assets/img/logo.png" alt="Logo Avada" class="my-2">
        <div class="d-flex align-items-center">
            <ul class ='d-flex align-items-center'>                    
                <li 
                    v-for='(item, index) in items' 
                    :key='index'
                    @click='getActiveLink(index)' 
                    class='ps-5'>
                    <a href="#" :class='menuActive==index ? "active" : ""'> {{ item.title }} </a>
                </li>
            </ul>
            <span class="px-2 ms-2">new</span>
            <a href="#" class="mx-5 px-4 py-2 ms-btn">Schedule a workout</a>
            <i class="fas fa-shopping-cart me-5"></i>
            <i class="fas fa-search"></i>
        </div>
    </nav>
 
</template>

<script>
export default {
    name: 'Nav',
    props: ['items'],
    data(){
        return {
            menuActive: 0
        }
    },
    methods: {
        getActiveLink: function(i) {
            return this.menuActive = i;
        }
    }
}
</script>

<style scoped lang='scss'>
    @import '../style/mixins.scss';
  
    .ms-wrap{
        @include my-wrap;

        ul {
            list-style: none;
            margin-bottom: 0rem;

            .active{
                color: white;
            }

            li{
                a{
                    color: #bcbcbc;
                    text-decoration: none;

                    &:hover{
                        color: white;
                    }
                }
            }
        }
        .fas{
            color: #bcbcbc;

            &:hover{
                color: white;
                cursor: pointer;
            }
        }

        span {
            display: block;
            border-radius: 2px;
            background-color: yellow;
            font-size: 0.9rem;
        }

        .ms-btn{
            font-size: 0.9rem;
            text-decoration: none;
            @include my-main-button;
        }
    }
</style>