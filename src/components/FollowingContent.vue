<template>
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
</template>

<script>
export default {

}
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
.my-card{
  min-width: 100px;
  min-height: 100px;
  border-radius: 20px;
  margin: 10px;
  position: relative;
}
.image{
  filter: brightness(80%);
}
.image:hover{
  filter: none;
}

.my-card p{
  z-index: 3;
  color: white;
  filter: contrast(100);
}
.bb{
  bottom: 10px;
}
.following-cards{
  display: grid;
  grid-template-columns: auto auto auto;
}
.username{
    bottom: 60px;
}
.account{
    bottom: 40px;
}
</style>