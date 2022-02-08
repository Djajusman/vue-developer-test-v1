<template>
  <div class="root">
    <div class="wrapper-main">
      <div class="left-align">
        <h2 class="bold center" style="color: #3aac5d">To Do list in Vue.js</h2>
      </div>
      <div v-for="item in comments" :key="item.id">
        <p class="fs-15 grey-label" style="margin-bottom: 0px">
          {{ item.name }}
        </p>
        <p>
          {{ item.content }}
          <span
            class="right fs-12 grey-label pointer"
            @click="clicklike(item.id)"
          >
            Like {{ item.like }}
          </span>
        </p>
      </div>
    </div>
    <label class="block fs-15 grey-label">name</label>
    <input
      type="text"
      v-model="newComment.name"
      style="border: 1px solid #73c000; border-radius: 4px; margin-bottom: 20px"
    />
    <label class="block fs-15 grey-label">Comment</label>
    <textarea
      v-model="newComment.content"
      v-on:keyup.enter="addComment()"
      class="textarea"
    ></textarea>
  </div>
</template>
<script>
export default {
  data() {
    return {
      likeid: 0,
      like: false,
      comments: [
        {
          name: 'lucy',
          content: 'Hi, edward wanna play?',
          time: '29 minutes ago',
          like: 2
        },
        {
          name: 'edward',
          content: 'Yes, I want to join to play',
          time: '27 minutes ago',
          like: 7
        },
        {
          name: 'lucy',
          content: 'When do you have free time',
          time: '26 minutes ago',
          like: 1
        }
      ],
      newComment: {
        name: '',
        content: ''
      },
      methods: {
        clicklike(id) {
          this.like = true
          this.likeid = id
        },
        addComment() {
          this.comments.push({
            id: 4,
            name: this.newComment.name,
            content: this.newComment.content,
            time: new Date(),
            like: 0
          })
          this.newComment.name = ' '
          this.newComment.content = ' '
        }
      },
      computed: {
        liked: function () {
          if (this.like) {
            for (var j = 0; j < this.comments.length; j++) {
              if (this.comments[j].id == this.likeid) {
                return this.comments[j].like + 1
                // break
              }
            }
          } else {
            this.comments.like
          }
        }
      }
    }
  }
}
</script>
