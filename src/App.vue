<template>
  <div id="app">
    <!-- Header -->
    <Header
      :menulinks='menuMain'
    />
    <!-- /Header -->

    <!-- Main -->
    <Main />
    <!-- /Main -->

    <!-- Footer -->
    <Footer 
    :posts='recentPosts'/>
    <!-- /Footer -->
  
    
  </div>
</template>

<script>
import Header from './components/Header';
import Main from './components/Main';
import Footer from './components/Footer';



export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
    
  },
  data() {
    return{
      menuMain: [
        {
          title: 'Home',
          url: ''
        },
        {
          title: 'Services',
          url: ''
        },
        {
          title: 'About',
          url: ''
        },
        {
          title: 'Videos',
          url: ''
        },
        {
          title: 'Blog',
          url: ''
        },
        {
          title: 'Store',
          url: ''
        }
      ],
      videos: [
        {
          url: './assets/video/video2-2x.jpg',
          title: 'Thighs & glute workout',
          subTitle: 'Increase your mobility'
        },
        {
          url: './assets/video/video7-2x.jpg',
          title: 'Lift, firm & perk up',
          subTitle: 'Feel young again'
        },
        {
          url: './assets/video/video9-2x.jpg',
          title: 'Slim & trim your waist',
          subTitle: 'Shed those extra pounds'
        }

      ],
      articles:[
        {
          url:'./assets/img/blog4-2x-400x258.jpg',
          title: 'The best protein shake',
          post: 'By admin | November 26th, 2019 | Gym'
        },
        {
          url:'./assets/img/blog1-2x-400x258.jpg',
          title: 'Ultimate cardio workout',
          post: 'By admin | November 26th, 2019 | Gym'
        },
        {
          url:'./assets/img/blog3-2x-400x258.jpg',
          title: 'New juices available now',
          post: 'By admin | November 26th, 2019 | Gym'
        },

      ],
      recentPosts: [
        {
          title: 'The best protein shake',
          url:''
        },
        {
          title: 'Ultimate cardio workout',
          url:''
        },
        {
          title: 'New juices available now',
          url:''
        },
        {
          title: 'Tips to find training partners',
          url:''
        },
        {
          title: '20 best healthy recipes',
          url:''
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  @import './style/general.scss';
</style>
