<template>
  <q-page padding class="major">
<div>

  <div class="lefter">
    <q-scroll-area
      :thumb-style="thumbStyle"
      :bar-style="barStyle"
      style="height: 80vh; width: 345px; padding-right: 15px;"
    >
      <div style="margin-left: 0;">
        <q-tabs 
              v-model="tab" 
              vertical
              indicator-color="transparent"
              active-color="pink"
              >
              <div class="trial" @click="tabhome" >
                <q-icon size="30px" name="home"></q-icon>
                <div :class="{active : isactive1}">home</div>
              </div>
              <div class="trial" @click="tabzy">
                <q-icon size="30px" name="people"></q-icon>
                <div :class="{active : isactive2}">following</div>
              </div>
              <div class="trial" @click="tablive">
                <q-icon size="30px" name="camera"></q-icon>
                <div :class="{active : isactive3}">live</div>
              </div>
              </q-tabs>
      </div>
      <q-separator />
      <div class="" style=" text-align: left;width: auto; padding: 10px 5px;">
                <p class="drawer-text3">
                  Log in to follow creators, like videos, and view comments.
                </p>
                <q-btn
                  outline
                  style="color: #FE2C55;margin:5px  0 ; width: 100%; padding: 11px 0; border-radius: 5px; text-transform: capitalize; font-weight: bold;font-size: larger; "
                  label="Log In"
                  @click="pop = true"
                />
              </div>

      <q-separator  />
              
               <div class="drawer-text3" style="padding: 10px 5px;font-size: 14px;opacity: .8;">Suggested Accounts</div>
  
                    <div class="suggested">
                      <div>
                        <q-avatar size="30px">
                          <img src="https://cdn.quasar.dev/img/avatar.png">
                        </q-avatar>
                      </div>
                      <div>
                        <div class="username">
                          diamondplatnumz
                        </div>
                        <div class="accname">
                          @platinumzofficial
                        </div>
                      </div>
                    </div>

                    <div class="suggested">
                      <div>
                        <q-avatar size="30px">
                          <img src="https://cdn.quasar.dev/img/avatar.png">
                        </q-avatar>
                      </div>
                      <div>
                        <div class="username">
                          diamondplatnumz
                        </div>
                        <div class="accname">
                          @platinumzofficial
                        </div>
                      </div>
                    </div>

                    <div class="suggested">
                      <div>
                        <q-avatar size="30px">
                          <img src="https://cdn.quasar.dev/img/avatar.png">
                        </q-avatar>
                      </div>
                      <div>
                        <div class="username">
                          diamondplatnumz
                        </div>
                        <div class="accname">
                          @platinumzofficial
                        </div>
                      </div>
                    </div>
                    <div class="suggested">
                      <div>
                        <q-avatar size="30px">
                          <img src="https://cdn.quasar.dev/img/avatar.png">
                        </q-avatar>
                      </div>
                      <div>
                        <div class="username">
                          diamondplatnumz
                        </div>
                        <div class="accname">
                          @platinumzofficial
                        </div>
                      </div>
                    </div>
                   
                    <div class="see" exact name="following" @click="tabzy">See more</div>


      <q-separator />

                <div class="drawer-text3" style="padding: 10px 5px;font-size: 14px;opacity: .8;">Discover</div>

                <div class="row drawer-text content-start">
                  <div class="tag"><span>#</span>kulosa</div>
                  <div class="tag"><span>#</span>fyp</div>
                  <div class="tag"><span>#</span>aaliyah</div>
                  <div class="tag"><span>#</span>topg</div>
                  <div class="tag"><span>#</span>funsize</div>
                  <div class="tag"><span>#</span>rush</div>
                  <div class="tag"><span>#</span>diy</div>
                  <div class="tag"><span>#</span>viral</div>
                  <div class="tag"><span>#</span>tittokKE</div>
                  <div class="tag"><span>#</span>muturaisnotafruit</div>
                  <div class="tag"><span>#</span>lowquality</div>
                  <div class="tag"><span>#</span>xyz</div>
                  <div class="tag"><span>#</span>foryourpage</div>
                  <div class="tag"><span>#</span>254</div>
                  <div class="tag"><span>#</span>gossip</div>
                  <div class="tag"><span>#</span>goviral</div>
                </div>


    </q-scroll-area>
  </div>
</div>




<div>

  <div class="righter">
    <div style=" height: 100%;">
      <q-tab-panels
          v-model="tab"
          animated
          swipeable
          vertical
          transition-prev="jump-up"
          transition-next="jump-up"
        >
          <q-tab-panel name="home" >
            <home-content/>
          </q-tab-panel>

          <q-tab-panel name="following">
            <following-content />
          </q-tab-panel>

          <q-tab-panel name="live">
            <div >Movies</div>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
          </q-tab-panel>
        </q-tab-panels>
    </div>
  </div>
</div>

   

<q-dialog v-model="pop" >
      <q-card style="width: 400px">
        <q-card-section align="center" style="font-weight: bold; font-size: 25px">
        
            Log in to TikTok
        
        </q-card-section>
        <q-card-section>
          <q-list>
            <q-item>
                <div class="login-type">
                  <!-- <q-icon name="img:https://cdn.quasar.dev/logo-v2/svg/logo.svg" size="25px"></q-icon> -->
                  <!-- <i class="fas fa-flag"></i> -->
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z"/></svg>
                  <div class="label">
                    Use QR-code
                  </div>
                </div>
            </q-item>
            <q-item>
              <div class="login-type">
                  <q-icon name="person" size="25px"></q-icon>
                  <div class="label">

                    Use Phone / email/ username
                  </div>
                </div>
            </q-item>
            <q-item>
              <div class="login-type">
                  <!-- <q-icon name="book" size="25px"></q-icon> -->
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M504 256C504 119 393 8 256 8S8 119 8 256c0 123.78 90.69 226.38 209.25 245V327.69h-63V256h63v-54.64c0-62.15 37-96.48 93.67-96.48 27.14 0 55.52 4.84 55.52 4.84v61h-31.28c-30.8 0-40.41 19.12-40.41 38.73V256h68.78l-11 71.69h-57.78V501C413.31 482.38 504 379.78 504 256z"/></svg>
                  <div class="label">

                    Continue with Facebook
                  </div>
                </div>
            </q-item>
            <q-item>
              <div class="login-type">
                  <!-- <q-icon name="search" size="25px"></q-icon> -->
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 488 512">! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc.<path d="M488 261.8C488 403.3 391.1 504 248 504 110.8 504 0 393.2 0 256S110.8 8 248 8c66.8 0 123 24.5 166.3 64.9l-67.5 64.9C258.5 52.6 94.3 116.6 94.3 256c0 86.5 69.1 156.6 153.7 156.6 98.2 0 135-70.4 140.8-106.9H248v-85.3h236.1c2.3 12.7 3.9 24.9 3.9 41.4z"/></svg>
                  <div class="label">

                    Continue with Google
                  </div>
                </div>
            </q-item>
            <q-item>
              <div class="login-type">
                  <!-- <q-icon name="plane" size="25px"></q-icon> -->
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z"/></svg>
                  <div class="label">

                    Continue with Twitter
                  </div>
                </div>
            </q-item>
            <q-item>
              <div class="login-type">
                  <q-icon name="apple" size="25px"></q-icon>
                  <div class="label">

                    Continue with Apple
                  </div>
                </div>
            </q-item>
            <q-item>
              <div class="login-type">
                  <!-- <q-icon name="camera" size="25px"></q-icon> -->
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M224,202.66A53.34,53.34,0,1,0,277.36,256,53.38,53.38,0,0,0,224,202.66Zm124.71-41a54,54,0,0,0-30.41-30.41c-21-8.29-71-6.43-94.3-6.43s-73.25-1.93-94.31,6.43a54,54,0,0,0-30.41,30.41c-8.28,21-6.43,71.05-6.43,94.33S91,329.26,99.32,350.33a54,54,0,0,0,30.41,30.41c21,8.29,71,6.43,94.31,6.43s73.24,1.93,94.3-6.43a54,54,0,0,0,30.41-30.41c8.35-21,6.43-71.05,6.43-94.33S357.1,182.74,348.75,161.67ZM224,338a82,82,0,1,1,82-82A81.9,81.9,0,0,1,224,338Zm85.38-148.3a19.14,19.14,0,1,1,19.13-19.14A19.1,19.1,0,0,1,309.42,189.74ZM400,32H48A48,48,0,0,0,0,80V432a48,48,0,0,0,48,48H400a48,48,0,0,0,48-48V80A48,48,0,0,0,400,32ZM382.88,322c-1.29,25.63-7.14,48.34-25.85,67s-41.4,24.63-67,25.85c-26.41,1.49-105.59,1.49-132,0-25.63-1.29-48.26-7.15-67-25.85s-24.63-41.42-25.85-67c-1.49-26.42-1.49-105.61,0-132,1.29-25.63,7.07-48.34,25.85-67s41.47-24.56,67-25.78c26.41-1.49,105.59-1.49,132,0,25.63,1.29,48.33,7.15,67,25.85s24.63,41.42,25.85,67.05C384.37,216.44,384.37,295.56,382.88,322Z"/></svg>
                  <div class="label">

                    Continue with Instagram
                  </div>
                </div>
            </q-item>
          </q-list>
        </q-card-section>
        <q-separator/>
        <q-card-section align="center">
          Don't have an account? <span style="color: hotpink" @click="nil">Sign up</span>
        </q-card-section>
      </q-card>
    </q-dialog>
  </q-page>
</template>

<script scoped>
import { ref } from 'vue';
import  { useQuasar } from 'quasar';
import HomeContent from 'src/components/HomeContent.vue';
import FollowingContent from 'src/components/FollowingContent.vue'
export default {
  components: { HomeContent, FollowingContent },
  setup(){
    const $q = useQuasar()
    return {
      alert (){
        $q.dialog({
          title: 'alert',
          message: '1,2,3',
          html:true
        })
      }
    }
  },
  data() {
    return {
      isactive1: true,
      isactive2: false,
      isactive3: false,
      activeColor:"#FE2C55",
      pop: false,
      tab: ref('home'),
      splitterModel: ref(25),
      suggested:{
        backgroundColor: 'red'
      },
      thumbStyle: {
        right: "4px",
        borderRadius: "5px",
        backgroundColor: "#33333320",
        width: "5px",
        opacity: 0.75,
        height: "30px",
      },

      barStyle: {
        right: "2px",
        borderRadius: "9px",
        backgroundColor: "#ffffff",
        width: "9px",
        opacity: 0.2,

      },
      classs:{
        display: "flex"
      }
    };
  },
  updated(){
      if(this.tab === 'home'){
        this.isactive = true
      }
  },
  methods:{
    tabzy(){
      this.tab = "following"
      this.isactive1 = false
      this.isactive2 = true
      this.isactive3 = false

    },
    tabhome(){
      this.tab = "home"
      this.isactive1 = true
      this.isactive2 = false
      this.isactive3 = false

    },
    tablive(){
      this.tab = "live"
      this.isactive1 = false
      this.isactive2 = false
      this.isactive3 = true

    }
  }
};
</script>
<style scoped>
 .active{
  color:#FE2C55
 }
.major{
  display: grid;
  grid-template-columns: 24vw auto;
  /* background: greenyellow; */
}
.lefter{
  /* background: red; */
  margin-left: 30px;
  padding-left: 10px;
  height: 100%;
  position: fixed

}
.righter{
  /* background: greenyellow; */
  margin-left: 10px;
  padding-left: 10px;
  height: 100%;
}


.trial{
  display: flex;
  justify-content: flex-start;
  align-items: center;
  /* background: blue; */
  width: 100%;
  margin-left: 0;
  padding: 10px 0;
  gap:10px;
  font-weight: bold;
  text-transform: capitalize;
  cursor: default;
  color: black;
}


.test{
  width: 330px;
}

.suggested{
  display: grid;
  grid-template-columns: .5fr 4fr;
  align-items: center;
  padding-left: 10px;
  margin-bottom: 8px;
}
.username{
  font-weight: bolder;
  font-size: small;
}
.accname{
  font-size: smaller;
}

.see{
  color: #FE2C55;
  font-size: 15px;
  font-weight: 500;
  padding-left: 10px;
  margin-bottom: 8px;
  cursor: pointer
}

.drawer-text3 {
  opacity: 0.6;font-size: larger;font-weight: light;
}
.tag {
  border: 0.25px solid rgba(175, 174, 174,.5);
  padding: 2px 7px;
  border-radius: 20px;
  margin: 3px;
  cursor: pointer;
  color: rgb(124, 124, 124);
}
.tag span{
  color: black;
  font-size: 18px;
  font-weight: 600;
  padding: 1px 5px;
}
.tag:hover {
  background: rgba(213, 213, 213,.2);
  transition: all .2s ease;
}

.login-type{
  width: 100%;
  padding: 6px 10px 6px 10px;
  display: grid;
  grid-template-columns: auto auto ;
  align-items: center;
  text-transform: capitalize;
  border: 1px solid #d3d3d380;
  border-radius: 3px;
}
.label{
  text-align: center;
  display: flex;
  justify-content: flex-start;
}
svg{
  width: 20px;
}
</style>
