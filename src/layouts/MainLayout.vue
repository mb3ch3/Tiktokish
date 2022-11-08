<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated >
      <div class=" head fit row wrap justify-center items-center ">
            <div>
              <q-avatar size="80px">
                <q-img src="../assets/img/1200px-TikTok_logo.svg.png"/>
              </q-avatar>
            </div>
        
        <div class="ss ">
          <q-input
            v-model="search"
            debounce="500"
            placeholder="Search accounts and videos"
            item-aligned
            input-class="ss"
          >
            <template v-slot:append>
              <q-icon name="search" />
            </template>
          </q-input>
        </div>

          <div>
            <q-btn color="white" text-color="black" icon="add" label="Upload" />
            <q-btn color="red" label="Log In" padding="6px 30px" style="margin: 0 10px"/>
            <q-btn-dropdown flat dropdown-icon="more" text-color="black" fab-mini >
              <q-list>
                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>
                      <q-icon name="A"/>
                      English
                    </q-item-label>
                  </q-item-section>
                </q-item>
    
                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>
                      <q-icon name="feedback"/>
                      Feedback and Help
                    </q-item-label>
                  </q-item-section>
                </q-item>
    
                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    
                    <q-item-label>
                        <q-icon name="keyboard"/>
                        Keyboard shortcuts
                      </q-item-label>
                  </q-item-section>
                </q-item>
    
                <q-item clickable v-close-popup @click="onItemClick">
                  <q-item-section>
                    <q-item-label>
                      <q-icon name=""/>
                      Dark Mode
                      <q-toggle
                        v-model="value"
                        color="gray"
                      />
                    </q-item-label>
                  </q-item-section>
                </q-item>
              </q-list>
            </q-btn-dropdown>
          </div>
      </div>
    </q-header>

    <!-- <q-footer class="foot" style="background-color: black">
      <q-tabs>
        <q-route-tab
          icon="home"
          to="/"
          exact
        />
        <q-route-tab
          icon="search"
          to="/settings"
          exact
        />
        <q-btn class="btn" color="white" text-color="black" glossy icon="add" ripple="true"/>
        <q-route-tab
          icon="message"
          to="/settings"
          exact
        />
        <q-route-tab
          icon="person"
          to="/"
          exact
        />
      </q-tabs>
    </q-footer> -->

    
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',
  data(){
    return{
      thumbStyle: {
        right: '4px',
        borderRadius: '5px',
        backgroundColor: '#333',
        width: '5px',
        opacity: 0.75
      },

      barStyle: {
        right: '2px',
        borderRadius: '9px',
        backgroundColor: '#e64ce6cc',
        width: '9px',
        opacity: 0.2
      }
    }
  },
  components: {
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
<style scoped>
  .head{
    background: white;
    color: black;
  }
  .ss{
    min-width: 250px;
  }
  .foot{
    display: flex;
    justify-content: center;
  }
  .btn{
    margin: 3px;
  }
  /* .lll{
    margin-top: 9vh;
  } */
  .drawer-text{
    margin: 2vh 3vh ;
  }
  .tag{
    border: 0.75px solid gray;
    padding: 2px 5px;
    border-radius: 20px;
    margin: 3px;
    cursor: pointer;
  }
  .tag:hover{
    background: darkgray;
    color: white;
    transition: all .4s ease-in;
  }
</style>
