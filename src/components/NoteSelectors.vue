<template>
  <div class="note-selectors">
  <note-selector 
    v-for="note in notes"
    v-bind:key="note.id"
    v-bind:note="note"
  />
    
  </div>
</template>

<script>
import NoteSelector from "./NoteSelector.vue";
export default {
  name: "note-selectors",
  components: {
    NoteSelector,
  },
  data: function () {
    return {
      notes: [
        { id: 1, body: "Test numero uno", timestamp: Date.now() },
        { id: 2, body: "Test numero dos", timestamp: Date.now() },
        { id: 3, body: "Test numero tres", timestamp: Date.now() },
        { id: 4, body: "Test numero cuatro", timestamp: Date.now() },
      ],
    };
  },
};
</script>