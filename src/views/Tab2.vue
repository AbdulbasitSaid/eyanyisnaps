<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Efanyi Snaps</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-fab vertical="bottom" horizontal="center" slot="fixed">
        <ion-fab-button @click="takePhoto()">
          <ion-icon :icon="camera"></ion-icon>
        </ion-fab-button>
      </ion-fab>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { camera, trash, close } from "ionicons/icons";

import { usePhotoGallery } from "@/composables/usePhotoGallery";
import {
  IonPage,
  IonHeader,
  IonFab,
  IonFabButton,
  IonIcon,
  IonToolbar,
  IonTitle,
  IonContent,
  // IonGrid,
  // IonRow,
  // IonCol,
  // IonImg,
} from "@ionic/vue";

export default {
  name: "Tab2",
  components: {
    IonPage,
    IonHeader,
    IonFab,
    IonFabButton,
    IonIcon,
    IonToolbar,
    IonTitle,
    IonContent,
    // IonGrid,
    // IonRow,
    // IonCol,
    // IonImg,
  },
  setup() {
    const { takePhoto } = usePhotoGallery();
    return {
      takePhoto,
      camera,
      trash,
      close,
    };
  },
};
</script>