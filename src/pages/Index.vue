<template>
  <q-page class="bg-grey-3 q-py-md q-px-lg" style="font-family:Lato, sans-serif">

    <!-- <q-img src="~assets/neil.jpg" rounded/> -->
    <section id="about">
    <heading>About</heading>

          <q-img src="~assets/neil.jpg" width="100px" style="float: left;" class="q-mr-md"/>
          <p>Hi, I'm Neil Newman, a PhD student in the UBC Computer Science department. My supervisor is <a href="http://www.cs.ubc.ca/~kevinlb/index.html">Kevin
            Leyton-Brown</a>. I am a member of the <a href="http://www.cs.ubc.ca/labs/beta/">Algorithms Lab</a> (formerly BETA) and the <a
            href="https://www.cs.ubc.ca/cs-research/lci">Laboratory for Computational Intelligence.</a></p>

          <p>My research interests lie at the intersection of Artifical Intelligence and Microeconomics; I have particularly focused on computational tools to facilitate and analyze complex auctions (mostly applied to spectrum auctions).</p>
         <p>
        I was awarded  an NSERC CGSD and a British Columbia Graduate Scholarship.
        I received the Exemplary Paper in the AI and Computation Track Award at EC'20, and was part of a large team that won the 2018 INFORMS Franz Edelman Award for Achievement in Operations Research and the Management Sciences. 
        I was an Associate Workflow Chair for AAAI'21.
         </p>

    </section>

    <section-separator/>

    <!--  Projects Section -->
    <section id="projects">
    <heading>Selected Projects</heading>

    <div>
      <p class="text-h5">Incentive Auction</p>
      <q-img src="~assets/interference.png" width="400px"/>

      <p>Over 13 months in 2016–17 the US Federal Communications Commission (FCC) conducted an <a href="https://www.fcc.gov/about-fcc/fcc-initiatives/incentive-auctions">Incentive Auction</a> to repurpose radio spectrum from broadcast television to wireless internet. 
      I helped design <a href="http://www.cs.ubc.ca/labs/beta/Projects/SATFC/">SATFC</a>, a specialized solver used in the auction to solve station repacking problems. 
      Through this work, I was one of a large team that won the <span style="font-weight: bold;">2018 INFORMS Franz Edelman Award for Achievement in Operations Research and the Management Sciences</span>.</p>

      <p class="text-h5">Kudu</p>
      <p><a href="http://kudu.ug/">Kudu</a> is a mobile market for agricultural trade in Uganda. It also has an <a href="https://play.google.com/store/apps/details?id=com.kudu.market&fbclid=IwAR1L_U7IguiA3YBlpW6ZPBUduQmfmbKw3Eixcgqd82W-wQ1Ihq5e8-VlMvE">Android Application</a>.</p>

      <p class="text-h5">The Positronic Economist</p>
      <p>The <a href="https://www.cs.ubc.ca/research/posec/"> Positronic Economist</a> is software designed to translate high-level mechanism descriptions into Bayesian Action Graph Games.</p>
    </div>
    </section>

    <section-separator/>

    <!--  Publications Section -->
    <heading>Publications</heading>
    <q-list separator>
      <q-item v-for="entry in bibEntries" :key="entry.TITLE">
        <publication :entry="entry" />
      </q-item>
    </q-list>

    <section-separator/>

    <heading>Education</heading>
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

    <section-separator/>

    <heading>Selected Employment</heading>
    <q-timeline color="secondary">
      <q-timeline-entry
        title="Auctionomics"
        subtitle="2015 - (Ongoing)"
        avatar="~assets/auctionomics.png"
      >
      <div>I do consulting work for <a href="http://www.auctionomics.com/">Auctionomics</a>, a company that specializes in specializes in high stakes auctions.</div>
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

    <section-separator/>

    <!-- <q-icon name="fab fa-github"/> -->
    <!--  Links Section -->
    <heading>Links</heading>
    <ul>
      <li><q-icon name="fab fa-github"/>&nbsp <a href="https://github.com/newmanne">Github</a></li>
      <li><i class="ai ai-google-scholar-square"></i>&nbsp <a href="https://scholar.google.ca/citations?hl=en&user=r-VhDbwAAAAJ">Google Scholar</a></li>
      <li><q-icon name="fab fa-linkedin"/>&nbsp <a href="https://www.linkedin.com/in/neil-newman-86008667">LinkedIn</a></li>
    </ul>

    <section-separator/>

    <!--  Contact Section -->
    <heading>Contact</heading>
    <contact/>

    <section-separator/>

    <heading>Miscellaneous</heading>
    <ul>
      <li>I am the lead programmer and associate designer of <a href="https://play.google.com/store/apps/details?id=com.bfbdev.bfb.android&hl=en">GONE</a>, a mobile
        game for Android on the Play Store.</li>
      <li>A quick LibGDX <a href="/statics/game/index.html">game</a> I made during my term as Beer Czar (organizing socials for graduate students).</li>
      <li>Here are some links to talks I gave at our department's social <a href="https://www.cs.ubc.ca/~udls/">Undistinguished Lecture Series (UDLS)</a>: 
          <ul>
          <li><a href="https://www.cs.ubc.ca/~udls/showTalk.php/2014-11-14">The Franklin Expedition: A Canadian Myth</a></li>
          <li><a href="https://www.cs.ubc.ca/~udls/showTalk.php/2017-05-05">Native Advertising and Content Marketing</a></li>
          <li><a href="https://www.cs.ubc.ca/~udls/showTalk.php/2018-10-12">Theranos</a></li>
          <li><a href="https://www.cs.ubc.ca/~udls/showTalk.php/2016-01-08">Science Fiction</a></li>
          <li><a href="https://www.cs.ubc.ca/~udls/showTalk.php/2015-09-11">Social Engineering</a></li>
          <li><a href="https://www.cs.ubc.ca/~udls/showTalk.php/2015-04-17">Tabletop Game Design</a></li>
          </ul>
      </li>
    </ul>

  </q-page>
</template>

<script>

  import BibtexParser from '../bibtex_js'
  import Publication from '../components/Publication'
  import Contact from '../components/Contact'
  import Heading from '../components/Heading'
  import SectionSeparator from '../components/SectionSeparator'

  export default {
    name: 'PageIndex',
    components: {
      Contact,
      Publication,
      Heading,
      SectionSeparator
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
