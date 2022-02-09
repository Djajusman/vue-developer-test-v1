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
      mounted: {
        listComment() {
          fetch('https://jsonplaceholder.typicode.com/posts/1/comments')
            .then((response) => response.json())
            .then((json) => console.log(json))
        }
      },
      methods: {
        storeComment() {
          fetch('https://jsonplaceholder.typicode.com/posts/1/comments', {
            method: 'POST',
            body: JSON.stringify({
              title: 'foo',
              body: 'bar',
              userId: 1
            }),
            headers: {
              'Content-type': 'application/json; charset=UTF-8'
            }
          })
            .then((response) => response.json())
            .then((json) => console.log(json))
        },

        removeComment() {
          fetch('https://jsonplaceholder.typicode.com/posts/1/comments', {
            method: 'DELETE'
          })
        },

        updateComment() {
          fetch('https://jsonplaceholder.typicode.com/posts/1/comments', {
            method: 'PUT',
            body: JSON.stringify({
              id: 1,
              title: 'foo',
              body: 'bar',
              userId: 1
            }),
            headers: {
              'Content-type': 'application/json; charset=UTF-8'
            }
          })
            .then((response) => response.json())
            .then((json) => console.log(json))
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
