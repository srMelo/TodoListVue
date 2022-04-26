<template>
  <div class="container">
    <h2 class="text-center mt-5">Lista de Tarefas</h2>
    <div class="d-flex">
      <input type="text" placeholder="Nova tarefa ..." class="form-control" />
      <button type="button" class="btn btn-info rounded-0">Adicionar</button>
    </div>

    <table class="table table-bordered mt-5">
      <thead>
        <tr>
          <th scope="col">Nome</th>
          <th scope="col">status</th>
          <th class="text-center" scope="col">#</th>
          <th class="text-center" scope="col">#</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(task, index) in tasks" :key="index">
          <td>{{task.Nome}}</td>
          <td>A cumprir</td>
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
  name: 'HelloWorld',
  props: {
    msg: String
  },

  data(){
    return {
      tasks: [
        {
          Nome: 'Ir para festa de Hanna',
          Status: 'A cumprir'
        },
        {
          Nome: 'Limpar a casa',
          Status: 'A cumprir'
        }
      ]
    }
  }
}

</script>


<style scoped>
</style>
