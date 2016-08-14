<template>
  <div id="toolbar">
    <i @click="$store.dispatch('addNote')" class="glyphicon glyphicon-plus"></i>
    <i @click="$store.dispatch('toggleFavorite')" class="glyphicon glyphicon-star" :class="{'starred' : active.favorite}"></i>
    <i @click="$store.dispatch('deleteNote')" class="glyphicon glyphicon-remove"></i>
  </div>
</template>

<script>
export default{
  computed: {
      active(){
        return this.$store.state.activeNote
      }
  }
}

</script>
