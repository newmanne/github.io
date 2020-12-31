<template>
  <q-page class="bg-grey-3">

    <span class="text-h3">About</span>
<!--    <q-avatar size="lg"><img src="~assets/neil.jpg"/></q-avatar>-->

    <p>Hi, I'm Neil Newman, a PhD student in the UBC Computer Science department. My supervisor is <a href="http://www.cs.ubc.ca/~kevinlb/index.html">Kevin
      Leyton-Brown</a>. I am a member of the <a href="http://www.cs.ubc.ca/labs/beta/">Algorithms Lab</a> (formerly BETA) and the <a
      href="https://www.cs.ubc.ca/cs-research/lci">Laboratory for Computational Intelligence.</a></p>


    <span class="text-h3">Links</span>
    <ul style="list-style-type: none;">
      <li><a href="https://github.com/newmanne"><span class="label"><i class="icon fa-github"></i> Github</span></a></li>
      <li><a href="https://scholar.google.ca/citations?hl=en&user=r-VhDbwAAAAJ" class="ai ai-google-scholar-square"><span
        class="label"> Google Scholar</span></a></li>
      <li><a href="https://www.linkedin.com/in/neil-newman-86008667"><span class="label"><i class="icon fa-linkedin"></i> LinkedIn</span></a></li>
    </ul>


    <span class="text-h3">Research</span>
    <p>I'm currently working on <a href="http://kudu.ug/">Kudu</a>, a mobile market for agricultural trade in Uganda. I am also researching the <a
      href="https://www.fcc.gov/about-fcc/fcc-initiatives/incentive-auctions">FCC Incentive Auction</a> and am a developer of <a
      href="http://www.cs.ubc.ca/labs/beta/Projects/SATFC/">SATFC</a>, a specialized solver for the station repacking problem that arises in the auction.
      Through this work, I was one of a large team that won the <span style="font-weight: bold;">2018 INFORMS Franz Edelman Award for Achievement in Operations Research and the Management Sciences</span>.
      I have also worked on <a href="https://www.cs.ubc.ca/research/posec/">The Positronic Economist</a>, a system for automatically generating compact game
      representations from high-level specifications of mechanisms.</p>

    <!--  Publications Section -->
    <span class="text-h3">Publications</span>
    <q-list separator>
      <q-item v-for="entry in bibEntries">
        <publication :entry="entry"/>
      </q-item>
    </q-list>

    <span class="text-h3">Education</span>
    <q-timeline color="secondary">
      <q-timeline-entry
        title="Doctor of Philosophy in Computer Science"
        subtitle="2017 - (Ongoing)"
        avatar="~assets/ubc.png"
        >
        <div>University of British Columbia</div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Master of Science in Computer Science"
        subtitle="2014 - 2017"
        avatar="~assets/ubc.png"
      >
        <div>University of British Columbia</div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Bachelor of Applied Science in Engineering Science"
        subtitle="2009 - 2014"
        avatar="~assets/uoft.jpg"
      >
        <div>University of Toronto</div>
        <div>Major in Electrical and Computer Engineering</div>
      </q-timeline-entry>
    </q-timeline>


    <span class="text-h3">Selected Employment</span>
    <q-timeline color="secondary">
      <q-timeline-entry
        title="Contractor for Auctionomics"
        subtitle="2015 - (Ongoing)"
        avatar="~assets/auctionomics.png"
      >
      </q-timeline-entry>

      <q-timeline-entry
        title="Graduate TA for CSPC 210 Software Construction"
        subtitle="2014 - 2015"
        avatar="~assets/ubc.png"
      >
        <div>University of British Columbia</div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Software Developer, Member Services at Ontario Teachers' Pension Plan"
        subtitle="May 2012 - August 2013"
        avatar="~assets/otpp.png"
      >
      </q-timeline-entry>
    </q-timeline>

    <!--  Contact Section -->
    <span class="text-h3">Contact</span>
    <contact/>

    <span class="text-h3">Other</span>
    <q-list>
      <q-item>Lead programmer and associate designer of <a href="https://play.google.com/store/apps/details?id=com.bfbdev.bfb.android&hl=en">GONE</a> a mobile
        game for android on the google play app store
      </q-item>
      <q-item><a href="https://www.cs.ubc.ca/~udls/">UDLS</a> (search my name)</q-item>
    </q-list>

  </q-page>
</template>

<script>

  import BibtexParser from 'vue-bibtex/src/bibtex_js.js'
  import Publication from '../components/Publication'
  import Contact from '../components/Contact'

  export default {
    name: 'PageIndex',
    components: {
      Contact,
      Publication
    },
    data: () => {
      return {
        bibEntries: null,
      }
    },
    mounted () {
      this.$axios.get('./statics/publications/pubs.bib').then((response) => {
          let b = new BibtexParser()
          b.setInput(response.data)
          b.bibtex()
          this.bibEntries = Object.values(b.getEntries()).sort((a, b) => b.YEAR - a.YEAR)
        }
      )
    }
  }
</script>
