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
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
import { matAllInbox } from "@quasar/extras/material-icons";
export default defineComponent({
  name: "MainLayout",
  data() {
    return {

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
.foot {
  display: flex;
  justify-content: center;
}
.btn {
  margin: 3px;
}
/* .lll{
    margin-top: 9vh;
  } */
.drawer-text {
  margin: 2vh 3vh;
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

.main-content {
  /* background: orange; */
  max-width: 83vw;
  padding-right: 50px;
  margin-inline: auto;
}
</style>
