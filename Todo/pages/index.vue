<template>
  <section class="container">
    <div>
      <app-logo/>
      <h1 class="title">
        TodoList
      </h1>
      <h2 class="subtitle">
        Tu Recordatorio Favorito
      </h2>
      <div class="links">
        <input type="text" v-model="message" class="form-control" placeholder="Recordar" name="" value=""><br>
        <button
          @click="object.push({message})"
          target="_blank"
          class="btn btn-lg btn-rounded btn-block btn-outline-success">Agregar</button>
      </div>
      <div class="">
        <ul id="v-for-object" class="demo">
          <li v-for="value in object" :key='value'>
            {{ value }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>



import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  },
  data(){
    return {
      object:['Fernando','Ruiz','velasco'],
      valor:''
    }
  }
}
</script>

<style>
  .container {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .form-control {
      width: 100%;
      padding: .375rem .75rem;
      font-size: .875rem;
      line-height: 1.5;
      background-color: #fff;
      border: 1px solid #e9ecef;
      border-radius: .25rem;
      transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out;
  }

  .btn {
      display: inline-block;
      text-align: center;
      vertical-align: middle;
      user-select: none;
      border: 1px solid transparent;
      padding: .375rem .75rem;
      font-size: .875rem;
      line-height: 1.5;
      border-radius: .25rem;
      transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out;
  }

  .btn-outline-success {
      color: #00c292;
      background-color: transparent;
      border-color: #00c292;
  }

  button, select {
      text-transform: none;
  }

  button, input, optgroup, select, textarea {
      margin: 0;
      font-family: inherit;
      font-size: inherit;
      line-height: inherit;
  }

  .btn-group-lg>.btn, .btn-lg {
      padding: .5rem 1rem;
      font-size: 1.09375rem;
      line-height: 1.5;
      border-radius: .3rem;
  }

  .btn-group-lg>.btn-rounded.btn, .btn-rounded.btn-lg {
      padding: .75rem 1.5rem;
  }

  .btn-block {
      display: block;
  }

  .title {
    font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }

  .subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
  }

  .links {
    padding-top: 15px;
  }
</style>
