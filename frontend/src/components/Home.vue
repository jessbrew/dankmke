<script setup>
const goTo = (path) => {
    window.location.hash = path;
};
</script>
<template>
    <v-img cover src="../../public/german_flag.png" height="300px" class="hero-banner">
        <div class="text-center text-white text-overlay">
            <h1 class="welcome-text">Willkommen!</h1>
            <h2 class="subtitle-1">Welcome to DANK Milwaukee – Promoting German-American culture through music, dance, and more!</h2>
        </div>
    </v-img>
    <v-container class="about-section py-6">
        <v-row justify="center">
            <v-col cols="12" md="10">
            <p class="text-body-1 text-center">
                <strong>DANK Milwaukee</strong> was founded in 1960 and is one of the chapters of 
                <a href="https://dank.org/" target="_blank">DANK National</a>. DANK Milwaukee participates in 
                many local events such as Germanfest, Maifest, several Oktoberfests, and more.
            </p>
            </v-col>
        </v-row>
    </v-container>


    <v-container class="pb-10">
    <v-row justify="center" align="stretch" dense>
        <v-col cols="12" md="4" class="pa-4">
        <v-card class="hover-card" @click="goTo('/choir')">
            <v-img src="../../public/singers.png" height="200px" cover></v-img>
            <v-card-title>Choir</v-card-title>
            <v-card-text>
            Learn more about our choir and how to join rehearsals or performances.
            </v-card-text>
        </v-card>
        </v-col>

        <v-col cols="12" md="4" class="pa-4">
        <v-card class="hover-card" @click="goTo('/adultdancers')">
            <v-img src="../../public/dancers.jpg" height="200px" cover></v-img>
            <v-card-title>Adult Dance Group</v-card-title>
            <v-card-text>
            Join our adult folk dancers and keep the traditions alive through movement.
            </v-card-text>
        </v-card>
        </v-col>

        <v-col cols="12" md="4" class="pa-4">
        <v-card class="hover-card" @click="goTo('/kinderdancers')">
            <v-img src="../../public/kinders.png" height="200px" cover></v-img>
            <v-card-title>Kinder Dance Group</v-card-title>
            <v-card-text>
                Our children's dance group will learn traditional dances in a fun, inviting environment.
            </v-card-text>
        </v-card>
        </v-col>
    </v-row>
</v-container>

</template>

<style scoped>
.hero-banner {
    width: 100vw;
}
.text-overlay {
    background-color: rgba(0, 0, 0, 0.4);
    width: 100%;
    padding: 60px 20px;
    height: 100%;
}
.welcome-text {
    font-size: 60px;
}

.about-section p {
  font-size: 18px;
  line-height: 1.6;
  max-width: 800px;
  margin: 0 auto;
  color: #333;
}
</style>