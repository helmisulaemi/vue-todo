<template>
    <div class="profile">
      <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-6">
                <div class="media text-start">
                    <img src="../assets/photo.jpg" class="user-pic me-3">
                    <div class="media-body">
                        <h5 class="mt-0">{{ firstName }} {{ lastName }}</h5>
                        <p>{{ bio }}</p>
                    </div>
                </div>
            </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import 'bootstrap/dist/css/bootstrap.css'
  
  export default {
    name: 'ProfileView',
    data: function () {
        return {
            firstName: 'Helmi',
            lastName: 'Sulaemi',
            bio: 'Will you do the same for me? Its time to face the music Im no longer your muse.'
        }
    },
    components: {
      // HelloWorld
    }
  }
  </script>

  <style scoped>
  .user-pic {
    float: left;
    border-radius: 200%;
    height: 80px;
    width: 80px;
  }
  </style>
  