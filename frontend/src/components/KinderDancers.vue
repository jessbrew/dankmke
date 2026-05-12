<script setup>
</script>

<template>
  <v-container class="py-6">
    <!-- Header -->
    <v-row justify="center" class="mb-6">
      <v-col cols="12" md="10" class="text-center">
        <h1 class="display-1 font-weight-bold mb-2">Kinder Dancers</h1>
        <p class="text-body-1">
          We’re looking for young dancers to be part of something special!
          The DANK Milwaukee Kinder Dancers group will celebrate German heritage through music, movement, and fun.
        </p>
      </v-col>
    </v-row>

    <!-- Photo Placeholder -->
    <v-row justify="center" class="mb-6">
      <v-col cols="12" md="10">
        <v-row dense>
          <v-col cols="12" sm="6" md="4" v-for="n in 3" :key="n" class="pb-4">
            <v-img :src="`/kids${n}.jpg`" height="200px" cover alt="Kinder Dance Placeholder" />
          </v-col>
        </v-row>
      </v-col>
    </v-row>

    <!-- Info Section -->
    <v-row justify="center" class="mb-6">
      <v-col cols="12" md="8">
        <v-card elevation="1" class="pa-4">
          <h2 class="headline font-weight-medium mb-2">Join the Fun!</h2>
          <p class="text-body-1">
            We’re currently forming a Kinder Dance group for children ages <strong>6 to 14</strong>.
            No experience is necessary — just a willingness to learn, move, and have fun!
          </p>
          <p class="text-body-1">
            Our group will participate in local German festivals and cultural events. Practices will begin once enough families express interest.
          </p>
          <p class="text-body-1">
            Interested? <a href="https://forms.gle/GypzzjzNg8Nxr3wGA" target="_blank">Sign up here</a> to be the first to hear about rehearsal dates and details!
          </p>
        </v-card>
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
