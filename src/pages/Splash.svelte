<script>
  import { navigate } from "svelte-routing";
  import { scale } from "svelte/transition";
  import { elasticInOut } from "svelte/easing";

  import { Plugins } from "@capacitor/core";

  const splitpane = document.querySelector("ion-split-pane");
  splitpane.disabled = true;

  setTimeout(() => {
    splitpane.disabled = false;
    navigate("/slides");
  }, 4000);

  console.log("CAPACITOR PLUGINS", Plugins);

  //  Plugins.Geolocation.getCurrentPosition().then(position => {
  //    console.log("POS", position);
  //  });

  /*
  Plugins.Share.share({
    title: "See cool stuff",
    text: "Really awesome thing you need to see right meow",
    url: "http://ionicframework.com/",
    dialogTitle: "Share with buddies"
  })
    .then(shareRet => {
      console.log("SHARE", shareRet);
    })
    .catch(error => {
      console.log("SHARE ERROR", error);
    });

    */
</script>

<style>
  img {
    width: 60%;
  }
</style>

<ion-header translucent>
  <ion-toolbar>
    <ion-title>Ionic UI Companion</ion-title>
  </ion-toolbar>
</ion-header>

<ion-content>
  <br />
  <br />
  <br />
  <div class="ion-text-center">
    <img
      src="assets/img/great-success.png"
      alt="Great success"
      in:scale={{ duration: 1900, easing: elasticInOut }} />

    <div in:scale={{ delay: 400, duration: 1900, easing: elasticInOut }}>
      Great success!
    </div>
  </div>

</ion-content>
