<template>
    <div>
      <h1>Add Content</h1>
      <form @submit.prevent="submitForm">
        <label for="title">Title:</label>
        <input type="text" id="title" v-model="title">
        
        <label for="description">Description:</label>
        <textarea id="description" v-model="description"></textarea>
        
        <button type="submit">Add Content</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Dashboard',
    data() {
      return {
        title: '',
        description: ''
      }
    },
    methods: {
      submitForm() {
        // Send data to server
        const data = {
          title: this.title,
          description: this.description
        };
        this.$http.post('/api/content', data)
          .then(response => {
            // Display success message and clear form
            alert('Content added successfully');
            this.title = '';
            this.description = '';
          })
          .catch(error => {
            // Display error message
            alert('Error adding content');
            console.log(error);
          });
      }
    }
  }
  </script>