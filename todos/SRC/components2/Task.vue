<template>
  <div class="container">
    <div class="task">
      <!-- title -->
      <div class="title">
        <h1>todos</h1>
        <input type="text" v-mode="todoName" @keyup.enter="addTodo">
      </div>
      <!-- form -->
      <div class="form">
        <input type="text" placeholder="New Task" />
        <button><i class="fas fa-plus"></i></button>
      </div>
      <!-- task lists -->
      <div class="taskItems">
        <ul>
          <li>
            <button>Learn Web Development</button>
            <button><i class="far fa-trash-alt"></i></button>
          </li>
          <li>
            <button>Watch netflix</button>
            <button><i class="far fa-trash-alt"></i></button>
          </li>
        </ul>
      </div>
      <!-- buttons -->
      <div class="clearBtns">
        <button>Clear completed</button>
        <button>Clear all</button>
      </div>
      <!-- pending task -->
      <div class="PendingTasks">
        <span>Pending Tasks: </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Task",
};
</script>