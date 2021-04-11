<template>
<div class="page">
  <JournalEntries :journal="journal" />
</div>
</template>

<script>
import JournalEntries from "../components/JournalEntries.vue"
export default {
  name: 'Home',
  components: {
    JournalEntries
  },
  computed: {
    journal() {
      return this.$root.$data.journal;
    },
  }
}
</script>

<style scoped>
  .page {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 50px;
  }

  .main{
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .items{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    font-size: 50px;
    padding: 20px;
  }

  .link {
    margin: 20px;
  }


  h1 {
    display: flex;
    font-size: 70px;
  }

  img {
    width: 50%;
    margin: 20px;
  }

  .footer {
    display: flex;
    justify-content: center;
    margin-top: 20px;
    bottom: 0;
    left: 41%;
    background-color: #262626;
    align-items: center;
    padding: 10px;
    width: 100%;
    text-decoration: none;
  }
</style>
