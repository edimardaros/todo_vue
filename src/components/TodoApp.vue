<template>
  <div class="container">
    <h2 class="text-center mt-5"> Hello!!!</h2>

    <!-- Input -->
    <div class="d-flex">
      <input type="text" placeholder="Insira a tarefa" class="form-control" />

      <button class="btn btn-warning rounded-0"> Cadastrar </button>
    </div>

    <!-- Task table -->
    <table class="table table-bordered mt-5">
      <thead>
        <tr>
          <th scope="col">Task</th>
          <th scope="col">Status</th>
          <th scope="col" class="text-center">#</th>
          <th scope="col" class="text-center">#</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(task, index) in tasks" :key="index">
          <td>{{task.name}}</td>
          <td>{{task.status}}</td>
          <td>
            <div class="text-center">
              <span class="fa fa-pen"></span>
            </div>
          </td>
          <td>
            <div class="text-center">
              <span class="fa fa-trash"></span>
            </div>
          </td>
        </tr>
      </tbody>
    
    </table>


    


  </div>
</template>

<script>
export default {
  name: "TodoApp",
  props: {
    msg: String
  },

  data(){
    return {
      tasks: [
        {
          name: 'Steal bananas from the store.',
          status: 'to-do',
        },
        {
          name: 'Eat 1kg chocolate in 1 hour.',
          status: 'in-progress'
        }
      ]


    }
  }
}
</script>