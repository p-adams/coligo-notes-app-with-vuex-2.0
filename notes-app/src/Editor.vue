<template>
  <div id="note-editor">
    <textarea
      :value="activeNoteText"
      @input="editNote"
      class="form-control">
    </textarea>
  </div>
</template>

<script>

export default {
    methods: {
        editNote(...args){
            this.$store.dispatch('editNote', ...args)
        }
    },
    computed: {
        activeNoteText(){
            console.log('active: ', this.$store.state.activeNote.text )
            return this.$store.state.activeNote.text
        }
    }
}
</script>