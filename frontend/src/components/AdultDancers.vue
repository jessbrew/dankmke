<script setup>
</script>

<template>
  <v-container class="py-6">
    <!-- Header -->
    <v-row justify="center" class="mb-6">
      <v-col cols="12" md="10" class="text-center">
        <h1 class="display-1 font-weight-bold mb-2">DANK Milwaukee Choir</h1>
        <p class="text-body-1">
          Join us in celebrating German-American culture through music!
          Our choir performs a variety of traditional and contemporary pieces at local festivals and events.
        </p>
      </v-col>
    </v-row>

    <!-- Video -->
    <v-row justify="center" class="mb-6">
      <v-col cols="12" md="8">
        <video controls style="width: 100%; border-radius: 8px;">
          <source :src="'/maypole-dancers.mp4'" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
      </v-col>
    </v-row>

    <!-- Rehearsal Info -->
    <v-row justify="center" class="mb-6">
      <v-col cols="12" md="8">
        <v-card elevation="1" class="pa-4">
          <h2 class="headline font-weight-medium mb-2">Rehearsals</h2>
          <p class="text-body-1">
            We rehearse <strong>2nd & 4th Tuesdays at 6:30 PM</strong> at the
            <a href="https://maps.app.goo.gl/gvDNeoJUhZdDXnuw6" target="_blank">German Fest Office</a> in Menomonee Falls.
            New singers are always welcome — no experience necessary!
          </p>
        </v-card>
      </v-col>
    </v-row>

    <!-- Photo Gallery -->
    <v-row justify="center" class="mb-6">
      <v-col cols="12" md="10">
        <v-row dense>
          <v-col cols="12" sm="6" md="4" v-for="n in 6" :key="n" class="pb-4">
            <v-img :src="`/dancers${n}.jpg`" height="200px" cover alt="Choir photo" />
          </v-col>
        </v-row>
      </v-col>
    </v-row>

    <!-- Signup -->
    <v-row justify="center">
      <v-col cols="12" md="8" class="text-center">
        <p class="text-body-1">
          Interested in singing with us? <a href="https://forms.gle/GypzzjzNg8Nxr3wGA" target="_blank">Sign up here</a> or come visit a Tuesday rehearsal!
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
a {
  color: #0056a3;
  text-decoration: underline;
}
a:hover {
  text-decoration: none;
}
</style>
