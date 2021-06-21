<template>
    <div>
        <div class="ms-wrap d-flex">
            <div class='d-flex flex-column align-items-center p-3 ms-container'>
                <img src="../assets/img/logo.png" alt="Logo Avada" class="mb-2" >
                <p class="py-3">Ac aliquam neque sagittis diam faucibus vitae purus turpis phasellus. Pellentesque consectetur amet purus ultrices mauris.</p>
                <div class="ms-socials d-flex justify-content-center">
                    <i class="fab fa-facebook-f px-2"></i>
                    <i class="fab fa-twitter px-2"></i>
                    <i class="fab fa-youtube px-2"></i>
                    <i class="fab fa-instagram px-2"></i>
                    <i class="fab fa-linkedin-in px-2"></i>
                </div>
            </div>
            <div class='d-flex flex-column align-items-center px-3 ms-container'>
                <h4 class="p-3">Recent Posts</h4>
                <a href="#" v-for='(post,index) in posts' :key='index' class='py-2'> <i class="fas fa-chevron-right me-2"></i> {{ post.title}} </a>
            </div>
            <div class='d-flex flex-column align-items-center px-3 ms-container'>
                <h4 class="p-3">Contact informations</h4>
                <p class='py-2'>4746 Tipple Road Michigan 48449</p>
                <div class='d-flex flex-column align-items-center my-4'>
                    <span>Mobile: 1.800.000.0000</span>
                    <span>Email: info@your-company.com</span>
                </div>
            </div>
        </div>
        <div class="ms-copyright py-5 text-center">
            <p>&copy; Copyright 2012 - 2020 | Avada them by <span>ThemeFusion</span>| All rights reserved | Powered by <span>WordPress</span></p>
        </div>
            
    </div>
</template>

<script>
export default {
    name: 'Footer',
    props: ['posts']

}
</script>

<style scoped lang='scss'>

    div{
        background-color: #060606;
        .ms-wrap{
            width: 70%;
            margin: 0 auto;

            .ms-container{
                width: calc(100% / 3);
                margin: 80px 0;

                p {
                    color:#bcbcbc;
                    text-align: center;
                }

                .ms-socials{
                    i{
                        color: #f04e4b;
                    }
                }

                h4 {
                    color:white;
                    text-transform: uppercase;
                }

                a{
                    color: white;
                    text-decoration: none;
                } 
            }
        }
    }
    .ms-copyright {
        border-top: 1px solid #78787a;
        p {
            margin-top: 1rem;
            color: #bcbcbc; 
        }
    }

    span {
        color: white;
    }
    

</style>