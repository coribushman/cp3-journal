<template>
  <div class="page">
    <h1>Create a Journal Entry</h1>
    <div class="add">
        <div class="form">
          <input v-model="newEntry.title" placeholder="Title">
          <p></p>
          <textarea name="text" rows="8" cols="80" v-model="newEntry.text" placeholder="Text"></textarea>
          <p></p>
          <textarea name="date" rows="1" cols="8" v-model="newEntry.date" placeholder="Date"></textarea>
          <p></p>
          <input v-model="newEntry.image" placeholder="Image URL">
          <button @click="upload">Upload</button>
        </div>
        <!-- <div class="upload" v-if="Object.keys(newEntry).length !== 0">
          <p>Your entry has been added!</p>
        </div> -->
      </div>
  </div>
</template>

<script>
  export default {
  name: 'Create',
  data() {
    return {
      newEntry: {
        id: 0,
        title: "",
        text: "",
        date: "",
        image: ""
      },
    }
  },
  methods: {
    upload() {
      this.newEntry.id = this.$root.$data.journal.length + 2;
      this.$root.$data.journal.push(this.newEntry);
    },
  }
}
</script>

<style scoped>
.page {
  margin: 30px;
}

</style>
