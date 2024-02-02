<template>
  <v-app id="home">
    <NavBar/>
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
            <h1 class="text-grey">Hello</h1>
            <h1 class="text-grey"> I'm Mayank Arora</h1>
            <span class="text-grey"> Full Stack Developer</span> <br>
            <v-btn title dark class="text-yellow mt-8" variant="outlined">
              Contact me
            </v-btn></div>
          </v-col>
          <v-col cols="2">
            <div style="position:absolute; z-index:9999;bottom:0;margin-left:auto;
            margin-right:auto; left:0;right:0;text-align:center">
            <v-icon>
              fas fa-angle-double-down 
            </v-icon>
             </div>
           </v-col>

          <v-col cols="5">
            <div style="position:relative; z-index:9999" class="mt-16">
              <v-img :src="require('@/assets/image.png')" alt="profile pic" contain max-height="300"></v-img>
            </div>

          </v-col>

        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                  <v-img :src="require('@/assets/image.png')" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16"> About me</h5>
              <div style="width:120px">
                <v-slider v-model="slider2" color="yellow" label="track-color">
            </v-slider>
              </div>
              <h4 class="mt-n4">I Am a Full Stack Developer</h4>
              <h4>And AI-ML enthusiast</h4>
              <p class="text-grey">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio similique impedit, labore debitis natus, vitae architecto officiis magni ratione aliquam, laboriosam voluptas ea! Tenetur sit nihil voluptatibus ab maxime aperiam praesentium velit mollitia eveniet? Suscipit eveniet, sed eum libero magnam magni inventore laborum quasi quia tempora nemo, porro aliquam explicabo!</p>
              <br>
              <p class="text-grey">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Explicabo doloremque aut sint temporibus obcaecati cupiditate totam incidunt reiciendis itaque, dignissimos vero quasi fuga deleniti. Tenetur dolores dicta, quae quaerat quas provident facere iste consectetur dolor necessitatibus eveniet est quibusdam harum eos, maxime odit voluptate placeat odio nisi nihil enim voluptatibus.

              </p>
              <v-btn tile dark color="yellow" class="mt-4">
                Download Resume
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What I Do</h2>
        <div style="width:120px; margin: 0 auto">
          <v-slider v-model="slider2" color="yellow" label="track-color"></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop" color="#FBDF7E"></v-btn>
                <h3 class="ml-3 mt-4">Web Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet.
                  <br>
                  Lorem, ipsum.
                </p>
              </div>

               <div class="child">
                <v-btn icon="fas fa-mobile-alt" color="#FBDF7E"></v-btn>
                <h3 class="ml-3 mt-4">App Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet.
                  <br>
                  Lorem, ipsum.
                </p>
              </div>

              <div class="child">
                <v-btn icon="fas fa-camera" color="#FBDF7E"></v-btn>
                <h3 class="ml-3 mt-4">Photography</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet.
                  <br>
                  Lorem, ipsum.
                </p>
              </div>

            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mr-2">All</v-btn>
          <v-btn class="mr-2">Web Design</v-btn>
          <v-btn class="mr-2">App Design</v-btn>
          <v-btn class="mr-2">Photography</v-btn>
          <v-btn variant="tonal">Illustration</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item,i) in items":key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering,props}">
                <v-card :elevation="isHovering?12:2" :class="{'on-hover': isHovering}" v-bind="props">
                  <v-img :src="item.img" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
            
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF73" class="mt-4">Load More</v-btn>
          </div>   
      </v-col>

      <v-col cols="12" id='page'>
              <div class="pre">
                <v-row>
                  <v-col cols="12" sm="4">
                    <v-card class="mw-auto" max-width="344" height="">
                      <v-img :src="require('@/assets/image2.jpg')" height="200px" cover></v-img>
                      <v-card-title>ABC</v-card-title>
                      <v-card-subtitle>
                        By Mayank | 15 Jan 2024
                      </v-card-subtitle>
                      <v-card-text>
                       Lorem, ipsum dolor sit amet consectetur adipisicing elit. Placeat, aspernatur?
                      </v-card-text>
                      
                    </v-card>
                  </v-col>

                   <v-col cols="12" sm="4">
                    <v-card class="mw-auto" max-width="344" height="">
                      <v-img :src="require('@/assets/image2.jpg')" height="200px" cover></v-img>
                      <v-card-title>ABC</v-card-title>
                      <v-card-subtitle>
                        By Mayank | 15 Jan 2024
                      </v-card-subtitle>
                      <v-card-text>
                       Lorem, ipsum dolor sit amet consectetur adipisicing elit. Placeat, aspernatur?
                      </v-card-text>
                      
                    </v-card>
                  </v-col>

                   <v-col cols="12" sm="4">
                    <v-card class="mw-auto" max-width="344" height="">
                      <v-img :src="require('@/assets/image2.jpg')" height="200px" cover></v-img>
                      <v-card-title>ABC</v-card-title>
                      <v-card-subtitle>
                        By Mayank | 15 Jan 2024
                      </v-card-subtitle>
                      <v-card-text>
                       Lorem, ipsum dolor sit amet consectetur adipisicing elit. Placeat, aspernatur?
                      </v-card-text>
                      
                    </v-card>
                  </v-col>
                </v-row>
              </div>
            </v-col>

            <v-col cols="12" id="blog">
              <div class="hire">
                <v-row>
                  <v-col cols="12" sm="8">
                    <h1 class="mt-9">Open to Work</h1>
                    <p class="text-grey">
                      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptate suscipit minus placeat ratione, temporibus nesciunt asperiores recusandae ducimus tempore iusto!

                    </p>
                  </v-col>
                  <v-col cols="12" sm="4">
                    <v-btn color="#F8DF73" class="mt-15">Hire me</v-btn>
                  </v-col>
                </v-row>
              </div>
            </v-col>
        <v-col cols="12" sm="12" class="px-16" id="contact">
          <v-row>
            <v-col cols="12" sm="4">
              <div class="child">
                <h1>Contact info</h1>
                <v-btn icon="fas fa-map-marker-alt" class="mt-10" variant="outlined"></v-btn> <br>
                <span class="text-caption">
                  Patiala
                </span><br>
                <v-btn icon="fas fa-phone-alt" class="mt-10" variant="outlined"></v-btn> <br>
                <span class="text-caption">83602-68092</span><br>
                <v-btn icon="fas fa-envelope" class="mt-10" variant="outlined"></v-btn> <br>
                <span class="text-caption">arora7827@gmail.com</span><br>
              </div>
            </v-col>
            <v-col cols="12" sm="8">
              <h1 class="mt-8"> Send your message</h1>
              <v-divider></v-divider>
              <span class="text-caption">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quidem libero sequi maxime voluptatibus totam possimus tempora facere ut in, aliquid sint. Minima, tempora adipisci. Enim molestias asperiores voluptatum assumenda commodi!

              </span>
              <v-row class="mt-10"> 
                <v-col cols="12" sm="6">
                  <v-text-field label="Name" persistant-hint variant="outlined"></v-text-field>
                </v-col>
            
                <v-col cols="12" sm="6">
                  <v-text-field label="Phone No" persistant-hint variant="outlined"></v-text-field>
                </v-col>
              </v-row>
                <v-textarea label="Message" persistant-hint variant="outlined"></v-textarea>
                <v-btn color="#FBDF7E" class="mt-2"> Submit Now</v-btn>
          
            </v-col>
          </v-row>
        </v-col>

    </v-container>
    <FooterView/>
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '@/components/NavBar.vue';
import FooterView from '@/components/FooterView.vue'

export default defineComponent({
  name: 'HomeView',
  setup(){
    return {
      slider2:50,
      items : [
        {
        img:""
        },
        {
        img:""
        },
        {
        img:""
        },
        {
        img:""
        },
        {
        img:""
        },
        {
        img:""
        },
        ]
    }
  },

  components: {
    NavBar,
    FooterView
  },
});
</script>
<style scoped>
.v-container{
  padding:16px 0;
}
.head {
  position: relative;
  text-align: center;
  padding:12px;
  margin: bottom 6px;
  height:400px;
  width:100%;
  color:white;


}
.head:before{
  content:" ";
  position: absolute;
  top:0;
  left:0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head:after{
  content:" ";
  position: absolute;
  top:0;
  right:0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}
.egg{
  display: block;
  margin-left:100px;
  margin-top:50px;
  width: 356px;
  height:300px;
  background-color:#fbdf7e;
  border-radius:50% 50% 50% 50% / 60% 60% 40% 0%;
}
.first{
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2 rem;
}
.child{
  display:inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.imgHover{
  padding:0 200px;
}
.pre{
  width:100%;
  height: 380px;
  text-align: center;
  padding :0 200px;
  background-color: #f5f5f5;

}

.hire{
  width: 100%;
  height:200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top:-24px;
}
</style>
