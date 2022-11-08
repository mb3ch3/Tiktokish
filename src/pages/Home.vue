<template>
  <q-page padding>
    <q-splitter
      v-model="splitterModel"
      style="height: 80vh"
    >
    <template v-slot:before>
      <div class="q-ma-md">
        <q-scroll-area
          :thumb-style="thumbStyle"
          :bar-style="barStyle"
          style="height: 75vh; max-width: 320px;"
        >
          <div class="fit row wrap justify-start" style="width: 100px">
            <q-tabs 
              v-model="tab" 
              vertical
              indicator-color="red"
              >
              <q-tab name="home" >
                <q-item exact>
                  <q-item-section avatar>
                    <q-icon name="home" />
                  </q-item-section>
                  <q-item-section>
                    <q-item-label>For You</q-item-label>
                  </q-item-section>
                </q-item>
              </q-tab>
              <q-tab name="following">
                <q-item exact>
                  <q-item-section avatar>
                    <q-icon name="people" />
                  </q-item-section>
                  <q-item-section>
                    <q-item-label>Following</q-item-label>
                  </q-item-section>
                </q-item>
              </q-tab>
              <q-tab name="live">
                <q-item exact>
                  <q-item-section avatar>
                    <q-icon name="camera" />
                  </q-item-section>
                  <q-item-section>
                    <q-item-label>Live</q-item-label>
                  </q-item-section>
                </q-item>
              </q-tab>
  
              <q-separator inset />
  
              <div class="row items-center justify-start" style="width: auto">
                <p class="drawer-text">
                  Log in to follow creators, like videos, and view comments.
                </p>
                <q-btn
                  outline
                  style="color: #FE2C55; margin: 1vh 3vh 2vh 3vh"
                  label="Log In"
                  padding="7px 6vw"
                  @click="pop = true"
                />
              </div>
  
              <q-separator inset />
  
              <q-tab>
                <q-item>
                  <q-item-label>
                    <div class="drawer-text2 ">Suggested Accounts</div>
                  </q-item-label>
                </q-item>
              </q-tab>
  
              <q-item>
                <q-list>
                  <q-item>
                    <q-item-section> Jane </q-item-section>
                  </q-item>
                  <q-item>
                    <q-item-section> Jane </q-item-section>
                  </q-item>
                  <q-item>
                    <q-item-section> Jane </q-item-section>
                  </q-item>
                  <q-item>
                    <q-item-label> See More </q-item-label>
                  </q-item>
                </q-list>
              </q-item>

              <q-tab>
                <q-item>
                  <q-item-label>
                    <div class="drawer-text3">Discover</div>
                  </q-item-label>
                </q-item>
              </q-tab>

              <q-item>
                <div class="row drawer-text content-start">
                  <div class="tag">#kulosa</div>
                  <div class="tag">#fyp</div>
                  <div class="tag">#aaliyah</div>
                  <div class="tag">#topg</div>
                  <div class="tag">#funsize</div>
                  <div class="tag">#rush</div>
                  <div class="tag">#diy</div>
                  <div class="tag">#viral</div>
                  <div class="tag">#tittokKE</div>
                  <div class="tag">#muturaisnotafruit</div>
                  <div class="tag">#lowquality</div>
                  <div class="tag">#xyz</div>
                  <div class="tag">#foryourpage</div>
                  <div class="tag">#254</div>
                  <div class="tag">#gossip</div>
                  <div class="tag">#goviral</div>
                </div>
              </q-item>
            </q-tabs>
          </div>
        </q-scroll-area>
        
        
      </div>
    </template>
    <template v-slot:after>
      <q-tab-panels
          v-model="tab"
          animated
          swipeable
          vertical
          transition-prev="jump-up"
          transition-next="jump-up"
        >
          <q-tab-panel name="home" >
            <div class="text-h4 q-mb-md">Mails</div>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
          </q-tab-panel>

          <q-tab-panel name="following">
            <div class="fit row wrap justify-start items-start content-start">
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
            <div class="text-h4 q-mb-md">Movies</div>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.</p>
          </q-tab-panel>
        </q-tab-panels>
    </template>
    </q-splitter>
    <q-dialog v-model="pop">
      <q-card>
        <q-card-section align="center">
          Log in to TikTok
        </q-card-section>
        <q-card-section>
          <q-list>
            <q-item>
              <q-item-section>
                <q-btn name="google" icon="code" outline label="Use QR Code"/>
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

<script>
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
      },

      barStyle: {
        right: "2px",
        borderRadius: "9px",
        backgroundColor: "#FFFFFF",
        width: "9px",
        opacity: 0.2,
      },
    };
  },
};
</script>
<style scoped>
.smally{
  width: 40px;
  height: 40px;
  border-radius: 50% !important;
  background: #FE2C55;
  bottom: 100px;
  left: 42.5%;

}

.username{
  bottom: 60px;
}
.account{
  bottom: 40px;
}
.bb{
  bottom: 10px;
}
.my-card{
  min-width: 250px;
  min-height: 300px;
  border-radius: 20px;
  margin: 30px;
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
.drawer-text {
  margin: 2vh 3vh;
}
.drawer-text2 {
  margin: 2vh 3vh 2vh -14vh;
}
.drawer-text3 {
  margin: 2vh 3vh 2vh -25vh;
}
.tag {
  border: 0.75px solid gray;
  padding: 2px 5px;
  border-radius: 20px;
  margin: 3px;
  cursor: pointer;
}
.tag:hover {
  background: darkgray;
  color: white;
  transition: all 0.4s ease-in;
}
</style>
