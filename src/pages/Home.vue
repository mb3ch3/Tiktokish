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
            <div >Mails</div>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
          </q-tab-panel>

          <q-tab-panel name="following">
            <div class="following-cards">
                <q-card class="my-card text-white">
                  <q-img class=" image" src="../assets/img/toll.png"/>
                  <div class="smally absolute-bottom" align="center"></div>
                  <p style="font-weight: bold;" class=" username absolute-bottom text-center">Burna Boy</p>
                  <p class=" account absolute-bottom text-center">burnaboyofficial</p>
                  <div class=" bb absolute-bottom" align="center">
                    <q-btn style="background: #FE2C55; color: white" ripple="true" label="FOLLOW" />
                  </div>
                </q-card>

                <q-card class="my-card text-white">
                  <q-video 
                  :ratio="0.795"
                  frameborder="0"
                  src="https://assets.mixkit.co/videos/preview/mixkit-going-down-a-curved-highway-through-a-mountain-range-41576-large.mp4"/>
                  <div class="smally absolute-bottom" align="center"></div>
                  <p style="font-weight: bold;" class=" username absolute-bottom text-center">Burna Boy</p>
                  <p class=" account absolute-bottom text-center">burnaboyofficial</p>
                  <div class=" bb absolute-bottom" align="center">
                    <q-btn style="background: #FE2C55; color: white" ripple="true" label="FOLLOW" />
                  </div>
                </q-card>

                <q-card class="my-card text-white">
                  <q-img class=" image" src="../assets/img/toll.png">
                  </q-img>
                  <div class="smally absolute-bottom" align="center"></div>
                  <p style="font-weight: bold;" class=" username absolute-bottom text-center">Burna Boy</p>
                  <p class=" account absolute-bottom text-center">burnaboyofficial</p>
                  <div class=" bb absolute-bottom" align="center">
                    <q-btn style="background: #FE2C55; color: white" ripple="true" label="FOLLOW" />
                  </div>
                </q-card>

                <q-card class="my-card text-white">
                  <q-video 
                  :ratio="0.795"
                  frameborder="0"
                  src="https://assets.mixkit.co/videos/preview/mixkit-going-down-a-curved-highway-through-a-mountain-range-41576-large.mp4"/>
                </q-card>
                <q-card class="my-card text-white">
                  <q-img class=" image" src="../assets/img/toll.png">
                  </q-img>
                  <p style="font-weight: bold;" class=" username absolute-bottom text-center">Burna Boy</p>
                  <p class=" account absolute-bottom text-center">burnaboyofficial</p>
                  <div class=" bb absolute-bottom" align="center">
                    <q-btn style="background: #FE2C55; color: white" ripple="true" label="FOLLOW" />
                  </div>
                </q-card>

                <q-card class="my-card text-white">
                  <q-video 
                  :ratio="0.795"
                  frameborder="0"
                  src="https://assets.mixkit.co/videos/preview/mixkit-going-down-a-curved-highway-through-a-mountain-range-41576-large.mp4"/>
                </q-card>
              
            </div>
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

   

    <q-dialog v-model="pop">
      <q-card>
        <q-card-section align="center">
        
            Log in to TikTok
        
        </q-card-section>
        <q-card-section>
          <q-list>
            <q-item>
              <q-item-section>
                <q-btn name="google" icon="code" class="test" outline label="Use QR Code"/>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section>
                <q-btn name="google" icon="person" outline label="Use Phone / email/ username"/>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section>
                <q-btn name="google" icon="book" outline label="Continue with Facebook"/>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section>
                <q-btn name="google" icon="search" outline label="Continue with Google"/>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section>
                <q-btn name="google" icon="plane" outline label="Continue with Twitter"/>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section>
                <q-btn name="google" icon="apple" outline label="Continue with Apple"/>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section>
                <q-btn name="google" icon="camera" outline label="Continue with Instagram"/>
              </q-item-section>
            </q-item>
          </q-list>
        </q-card-section>
        <q-separator/>
        <q-card-section align="center">
          Don't have an account? <span style="color: pink" @click="nil">Sign up</span>
        </q-card-section>
      </q-card>
    </q-dialog>
  </q-page>
</template>

<script scoped>
import { ref } from 'vue';
import  { useQuasar } from 'quasar';
export default {
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
      this.isactive2 = fasle
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
.following-cards{
  display: grid;
  grid-template-columns: auto auto auto;
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
.smally{
  width: 40px;
  height: 40px;
  border-radius: 50% !important;
  background: #FE2C55;
  bottom: 100px;
  left: 42.5%;

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
.bb{
  bottom: 10px;
}
.my-card{
  min-width: 100px;
  min-height: 100px;
  border-radius: 20px;
  margin: 10px;
  position: relative;
}
.my-card p{
  z-index: 3;
  color: white;
  filter: contrast(100);
}
.image{
  filter: brightness(80%);
}
.image:hover{
  filter: none;
}

.drawer-text2 {
  margin: 2vh 3vh 2vh -14vh;
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
</style>
