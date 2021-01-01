<template>
  <q-layout view="lHh Lpr lff" class="shadow-2 rounded-borders">
    <q-header elevated class="bg-cyan-8">
      <link rel="stylesheet" href="/statics/css/academicons.min.css"/>
      <q-toolbar>
        <q-toolbar-title>Neil Newman</q-toolbar-title>
        <!-- <q-btn flat @click="right = !right" round dense icon="menu"/> -->
      </q-toolbar>
    </q-header>

    <!-- <q-drawer show-if-above v-model="right" side="right" bordered> -->
      <!-- drawer content -->
    <!-- </q-drawer> -->

    <q-page-container>
      <router-view/>
    </q-page-container>

  </q-layout>
</template>

<script>
  export default {
    data () {
      return {
        right: false
      }
    }
  }
</script>
