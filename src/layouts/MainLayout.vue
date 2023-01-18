<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated>
      <div class="head">
        <div class="aa">
          <q-img class="image" src="../assets/img/1200px-TikTok_logo.svg.png" />
        </div>

        <div>
          <q-input
            rounded
            dense
            clearable
            v-model="text"
            label="Search accounts and videos"
            standout="bg-deep-orange-1 text-dark"
          >
            <template v-slot:append>
              <q-icon name="search" @click="text = ''" class="cursor-pointer" />
            </template>
          </q-input>
        </div>

        <div>
          <q-btn color="white" text-color="black" icon="add" label="Upload" />
          <q-btn
            color="red"
            label="Log In"
            padding="6px 30px"
            style="margin: 0 10px"
            @click="pop = true"
          />
          <q-btn-dropdown
            flat
            dropdown-icon="more_vert"
            text-color="black"
            fab-mini
          >
            <q-list>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>
                    <q-icon name="A" />
                    English
                  </q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>
                    <q-icon name="feedback" />
                    Feedback and Help
                  </q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>
                    <q-icon name="keyboard" />
                    Keyboard shortcuts
                  </q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>
                    <q-icon name="" />
                    Dark Mode
                    <q-toggle v-model="value" color="gray" />
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

    <q-page-container class="main-content">

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

      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
import {fasFlag} from '@quasar/extras/fontawesome-v6'
export default defineComponent({
  name: "MainLayout",
  data() {
    return {
        pop: false,
      thumbStyle: {
        right: "4px",
        borderRadius: "5px",
        backgroundColor: "#333",
        width: "5px",
        opacity: 0.75,
      },

      barStyle: {
        right: "2px",
        borderRadius: "9px",
        backgroundColor: "#e64ce6cc",
        width: "9px",
        opacity: 0.2,
      },
      more: '<i class="ri-more-2-fill"></i>',
    };
  },
  components: {},

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
<style scoped>
svg{
  width: 20px;
}
.head {
  background: white;
  color: black;
  display: flex;
  /* grid-template-columns: 1.5fr 2fr 2fr; */
  align-items: center;
  justify-content: center;
  gap: 2vw;
}

.head div:nth-child(1) {
  display: flex;
  justify-content: flex-end;
}
.head div:nth-child(2) {
  min-width: 20vw;
  margin: 10px 150px 10px 100px;
}
.head div:nth-child(3) {
}
.image {
  height: auto;
  width: 120px;
}

.main-content {
  /* background: orange; */
  max-width: 83vw;
  padding-right: 50px;
  margin-inline: auto;
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
</style>
