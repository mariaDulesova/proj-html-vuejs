<template>
    <div>
        <nav class='d-flex justify-content-between align-items-center ms-wrap py-4'>
            <img src="../assets/img/logo.png" alt="Logo Avada" class="my-2">
            <div class="d-flex align-items-center">
                <ul class ='d-flex align-items-center'>
                    <li 
                        v-for='(link, index) in menulinks' 
                        :key='index'
                        @click='getActiveLink(index)' 
                        class='ps-5'>
                        <a href="#" :class='menuActive==index ? "active" : ""'> {{ link.title }} </a>
                    </li>
                </ul>
                <span class="px-2 ms-2">new</span>
                <a href="#" class="mx-5 px-4 py-2 ms-btn">Schedule a workout</a>
                <i class="fas fa-shopping-cart me-5"></i>
                <i class="fas fa-search"></i>
            </div>
        </nav>
    </div>
    
</template>

<script>
export default {
    name: 'Nav',
    props: ['menulinks'],
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
    div{
        background-color: #060606;

        .ms-wrap{
            width: 70%;
            margin: 0 auto;

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
                background-color: #4154fe;
                border-radius: 20px;
                color: white;
                text-decoration: none;
                font-size: 0.9rem;
                transition: all 0.3s;

                &:hover{
                    background-color: #f04e4b;
                }
            }

        }
    }
    

</style>