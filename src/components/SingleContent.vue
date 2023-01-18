<template>
  <div class="content">
    <q-avatar size="55px" class="avatar">
        <img src="https://cdn.quasar.dev/img/avatar.png"/>
    </q-avatar>
    <div class="middle">
        <div class="heading">
            <span class="username">diamondplatinum___z</span>
            <span class="acccname">platinumuztz234</span>
        </div>
        <div>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vel non corrupti impedit delectus ipsa eos dolor amet adipisci praesentium quisquam architecto nemo voluptatibus ab accusantium dicta, dolorum laborum maiores in?
        </div>
        <div>
            <!-- <iframe src="https://giphy.com/embed/IRFQYGCokErS0" width="360" height="500" frameBorder="0" class="giphy-embed video" allowFullScreen></iframe> -->
            <!-- <q-video src="https://www.pexels.com/video/repetitive-footage-of-a-woman-holding-a-mirror-ball-3444227/" /> -->
            <!-- <q-video :ratio="16/17" src="https://giphy.com/embed/IRFQYGCokErS0"></q-video> -->
            <video width="300" height="500" controls autoplay muted loop playsinline>
                <source src="../assets/video.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </div>
    </div>
    <div class="follow">
        <q-btn size="11px"  outline style="color: #FE2C55;" label="Follow" />
    </div>
  </div>
</template>

<script>

window.addEventListener('load', videoScroll);
window.addEventListener('scroll', videoScroll);

function videoScroll() {

  if ( document.querySelectorAll('video[autoplay]').length > 0) {
    var windowHeight = window.innerHeight,
        videoEl = document.querySelectorAll('video[autoplay]');

    for (var i = 0; i < videoEl.length; i++) {

      var thisVideoEl = videoEl[i],
          videoHeight = thisVideoEl.clientHeight,
          videoClientRect = thisVideoEl.getBoundingClientRect().top;

      if ( videoClientRect <= ( (windowHeight) - (videoHeight*.5) ) && videoClientRect >= ( 0 - ( videoHeight*.5 ) ) ) {
        thisVideoEl.play();
      } else {
        thisVideoEl.pause();
      }

    }
  }

}
</script>



<style scoped>
.content{
    height: 90vh;
    display:grid;
    grid-template-columns: 1fr 3fr 1fr;
    padding: 10px;
}

.avatar{
    justify-self: flex-end;
    margin-right: 15px;
    margin-top: 10px;

}
.follow{
    justify-self: center;
    margin-top: 10px;

}
.middle{
    display: grid;
    grid-template-columns: auto;
    grid-template-rows: .1fr auto 3fr;
    justify-content: flex-start;
}
.middle div{
    /* border: 1px hotpink solid; */
}

.heading{
    display: flex;
    gap: 5px;
    align-items: center;
}
.username{
    font-weight: bolder;
    font-size: 18px;
}
.video{
    border: 2px solid;
}

</style>