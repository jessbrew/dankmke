<script setup>
import {ref, computed} from 'vue';
import Home from './components/Home.vue';
import Choir from './components/Choir.vue';
import AdultDancers from './components/AdultDancers.vue';
import KinderDancers from './components/KinderDancers.vue';

const routes = {
  '/': Home,
  '/choir': Choir,
  '/adultdancers': AdultDancers,
  '/kinderdancers': KinderDancers
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
    currentPath.value = window.location.hash;
})

const currentView = computed(() => {
    return routes[currentPath.value.slice(1) || '/'] || NotFound;
})

const goTo = (path) => {
    window.location.hash = path;
};
</script>


<template>
<v-app>
    <v-app-bar color="#dce1e6" prominent  height="110">
        <div class="d-flex align-center clickable" @click="goTo('/')">
            <img src="./assets/dankLogo.png" class="dankLogo" />
        
            <div class="dankTitleGroup">
                <div class="dankTitle">German American National Congress - Milwaukee</div>
                <div class="subtitle">Deutsch Amerikanischer National Kongress</div>
            </div>
        </div>
        <v-spacer></v-spacer>
        <div class="navButtonGroup">
            <v-btn text @click="goTo('/choir')" class="navBtn">Choir</v-btn>
            <v-btn text @click="goTo('/adultdancers')" class="navBtn">Adult Dancers</v-btn>
            <v-btn text @click="goTo('/kinderdancers')" class="navBtn">Kinder Dancers</v-btn>
        </div>
    </v-app-bar>
    <v-main class="mainContent">
        <component :is="currentView"></component>
    </v-main>
    <v-footer color="#003399" app padless>
        <v-container class="py-4" fluid>
            <p class="footerText">
            © 2025 DANK Milwaukee — All rights reserved.
            </p>
        </v-container>
    </v-footer>
</v-app>
</template>

<style>
.clickable {
  cursor: pointer;
}
.dankLogo {
    max-height: 100px;
    padding-left: 10px;
    margin-right: 20px;
}
.dankTitleGroup {
  display: flex;
  flex-direction: column;
  justify-content: center;
  line-height: 1.2;
}
.dankTitle {
  font-family: 'Merriweather', serif;
  font-size: 30px;
  letter-spacing: 1px;
  font-weight: 700;
}
.subtitle {
  font-family: 'Merriweather', serif;
  font-size: 18px;
  font-weight: 300;
  color: #5a6e7f; 
  margin-right: 12px;
}

.navButtonGroup {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-right: 100px;
}
.navBtn {
  color: #5a6e7f;
  font-weight: 500;
  text-transform: none;
}
.footerText {
  font-size: 14px;
  color: #CBD5E1;
}
</style>