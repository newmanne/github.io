<template>
  <div>
    <p>
      newmanne at cs dot ubc dot ca<br/>
      ICICS Room X560<br/>
      289-2366 Main Mall<br/>
      Vancouver, British Columbia, Canada <br/>
    </p>
    <div class="google-maps">
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2603.721475094903!2d-123.24648697141113!3d49.262724866167446!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x548672cbd037e16d%3A0x4863aaf177384ea9!2sICICS+Computer+Science%2C+The+University+of+British+Columbia%2C+2366+Main+Mall%2C+Vancouver%2C+BC+V6T+1Z4!5e0!3m2!1sen!2sca!4v1420692915598"
      style="border:0" frameborder="0" height="450" width="600" class="q-pb-md"></iframe>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Contact'
  }
</script>

<style scoped>
    /* https://www.labnol.org/internet/embed-responsive-google-maps/28333/ */
    .google-maps {
        position: relative;
        padding-bottom: 75%; 
        height: 0;
        overflow: hidden;
    }
    .google-maps iframe {
        position: absolute;
        top: 0;
        left: 0;
        width: 100% !important;
        height: 100% !important;
    }
</style>
