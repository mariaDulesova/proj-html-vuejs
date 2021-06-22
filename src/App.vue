<template>
  <div id="app">
    <!-- Header -->
    <Header
      :menulinks='menuMain'
    />
    <!-- /Header -->

    <!-- Main -->
    <Main 
      :videoLinks='videos'
      :articleLinks='articles'
      :sponsorLinks='sponsors'
    />
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
          url: 'video2-2x',
          title: 'Thighs & glute workout',
          subTitle: 'Increase your mobility'
        },
        {
          url: 'video7-2x',
          title: 'Lift, firm & perk up',
          subTitle: 'Feel young again'
        },
        {
          url: 'video9-2x',
          title: 'Slim & trim your waist',
          subTitle: 'Shed those extra pounds'
        }

      ],
      articles:[
        {
          url:'blog4-2x-400x258',
          title: 'The best protein shake',
          post: 'By admin | November 26th, 2019 | Gym'
        },
        {
          url:'blog1-2x-400x258',
          title: 'Ultimate cardio workout',
          post: 'By admin | November 26th, 2019 | Gym'
        },
        {
          url:'blog3-2x-400x258',
          title: 'New juices available now',
          post: 'By admin | November 26th, 2019 | Gym'
        },

      ],
      sponsors: [
        {
          label:'sponsor-1-2x-200x103',
          name: 'Yoga Studio',
          description:'Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.',
          link:'Visit Yoga Studio'
        },
        {
          label:'sponsor-2-2x-200x103',
          name: 'Fitness Center',
          description:'Feugiat etiam dui mauris pharetra mauris sed pharetra. Convallis sapien ornare cras faucibus nulla porta dui a.',
          link:'Join Fitness Center'
        },
        {
          label:'sponsor-3-2x-200x103',
          name: 'Fitness Club',
          description:'Nisl at quam adipiscing montes, nec, adipiscing commodo aliquam tincidunt. Ligula in habitant et sagittis imperdiet.',
          link:'Learn about FC'
        },
        {
          label:'sponsor-4-2x-200x103',
          name: 'Power Gym',
          description:'Proin in viverra maecenas et mattis ut nibh enim. Gravida ultricies mi porta lacus. Et posuere velit sed nec eleifend.',
          link:'Visit Power Gym'
        }
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
