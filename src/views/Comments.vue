<template>
  <div id="app" class="container">
    <h1>Comment List</h1>

    <div v-if="!isEditing">
      <input type="text" v-model="comment" />
      <input type="submit" value="Add" @click="storeComment" />
    </div>
    <div v-else>
      <input type="text" v-model="comment" />
      <input type="submit" value="Update" @click="updateComment" />
    </div>
    <ol>
      <li v-for="(comment, index) in comments" :key="comment.id">
        {{ comment }}
        <button @click="editComment(index, comment)">Edit</button>
        <button @click="removeComment(index)">Delete</button>
      </li>
    </ol>
  </div>
</template>
<script>
export default {
  data() {
    return {
      data: {
        isEditing: false,
        comment: '',
        comments: [],
        selectedComment: null
      },

      methods: {
        storeComment() {
          this.comments.push(this.comment)
          this.comment = ''
        },

        removeComment(index) {
          this.comments.splice(index, 1)
        },

        updateComment() {
          this.comments.splice(this.selectedIndex, 1, this.comment)
          this.comment = ''
          this.isEditing = false
        },

        editComment(index, comment) {
          this.isEditing = true
          this.comment = comment
          this.selectedIndex = index
        }
      }
    }
  }
}
</script>
