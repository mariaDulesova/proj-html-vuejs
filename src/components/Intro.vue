<template>
  <section class='pb-5'>
    <div class='ms-wrap d-flex flex-column justify-content-center align-items-center pb-5'>
      <div class="d-flex justify-content-between ms-services mb-5">
        <div v-for="(service, index) in services" :key='index' class="ms-container">
          <div class="ms-img-container position-relative ">
            <img :src="require(`../assets/img/${service.name}.jpg`)" :alt="`${service.title}`">
            <div class="position-absolute bottom-0 start-0 pt-5 ps-2 pb-2 ms-text-absolute">
              <h4 class="ms-3">{{ service.title }}</h4>
              <p class="ms-3">{{ service.subTitle }}</p>
            </div> 
          </div> 
        </div>
      </div>
      <q class="text-center my-5">How you respond to the challenge in the second half will determine what you become after the game, whether you are a winner or a loser.</q>
      <img src="../assets/img/wave.png" alt="Wave" width='80' class="my-3">
      <div class="d-flex justify-content-center align-items-center ms-avatar mb-5">
        <img src="../assets/img/avatar-1-2x.jpg" alt="Avatar" class="me-3">
        <h5 class="me-3">Brad Johnson</h5>
        <p>Las Vegas</p>
      </div>
    </div>
  </section>    
</template>

<script>
export default {
    name: 'Intro',
    data() {
      return {
        services: [
          {
            name: 'service6-2x',
            title: 'Crossfit workout',
            subTitle: 'Push your limits'
          },
          {
            name: 'box1-2x',
            title: 'New gym apparel',
            subTitle: 'Look good, feel good'
          },
          {
            name: 'box3-2x',
            title: 'Team training',
            subTitle: 'Find a partner'
          }

        ]
      }
    }
}
</script>

<style scoped lang='scss'>
  @import '../style/mixins.scss';

  section {
    background-image: linear-gradient(to bottom right, #0517DE 20%, #bc0428);

    .ms-wrap {
    @include my-wrap;
    }

    q {
      font-size: 3rem;
      color: white;
      width: 90%;
    }

    .ms-services {
      .ms-container {
        width: calc(90% / 3);

        .ms-img-container{
          margin-top: -110px;
          border-radius: 10px 10px 70px 10px;
          overflow: hidden;
        }
      }

      img {
        width: 100%;
        overflow: hidden;
        //transition: all 0.2s;
      }
    
      .ms-text-absolute{
        width: 100%;
        background: linear-gradient( rgba(255, 255, 255, 0), rgba(0, 0, 0, 0.932));
      
        h4 {
          color: white;
          font-size: 2rem;
          letter-spacing: 1px;
        }
        p {
          color: yellow;
          font-size: 1.5rem;
        }

      }
    }
    
    .ms-avatar{
      img{
        width: 60px;
        border-radius: 50%;
      }
      h5 {
        margin-top: 0.5rem;
        color: white;
      }
      p {
        margin-top: 1rem;
        color:#bcbcbc;
        font-size: 17px;
      }
    }
  }
</style>