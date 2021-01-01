<template>
  <div>
    <span class="title text-bold">{{ entry.TITLE }}</span>,
    <div class="author">
      <span v-if="entry.AUTHOR" v-html="boldMe(entry.AUTHOR)"/>
    </div>
    <div>
      <span v-if="entry.JOURNAL"><em><span class="journal">{{ entry.JOURNAL }}</span></em>, </span>
      <span v-else-if="entry.BOOKTITLE"><em><span class="journal">{{ entry.BOOKTITLE }}</span></em>, </span>
      <span v-if="entry.LOCATION"><span class="location">{{ entry.LOCATION }}</span>, </span>
      <span v-if="entry.VOLUME"><span class="volume">vol. {{ entry.VOLUME }}</span>, </span>
      <span v-if="entry.NUMBER"><span class="number">no. {{ entry.NUMBER }}</span>, </span>
      <span v-if="entry.PAGES"><span class="pages">pp. {{ entry.PAGES }}</span>, </span>
      <span v-if="entry.MONTH"><span class="month">{{ entry.MONTH }}</span>, </span>
      <span v-if="entry.YEAR"><span class="year">{{ entry.YEAR }}</span>.</span>
      <span v-else>.</span>
      <span v-if="entry.NOTE"><br/><span class="note text-red">{{ entry.NOTE }}</span></span>

      <div>
        <template v-if="entry.FILE"><a :href="'/statics/publications/' + entry.FILE" target="_blank">[pdf]</a>&nbsp</template>
        <template v-if="entry.TALK"><a :href="entry.TALK">[talk]</a>&nbsp</template>
        <a v-if="entry.DOI" :href="' https://doi.org/' + entry.DOI">[doi]</a>
        <!-- <a role="button" data-toggle="collapse" :href="'#' + entry.BIBTEXKEY + '-bib'" aria-expanded="false" :aria-controls="entry.BIBTEXKEY + '-bib'">
          [bib]
        </a> -->
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Publication',
    props: {
      entry: {
        type: Object,
        required: true,
      }
    },
    methods: {
      boldMe: function (value) {
        if (!value) return ''
        return value.replace('Newman, Neil', '<span class="text-italic">Newman, Neil</span>')
      }
    },
  }
</script>

<style scoped>

</style>
