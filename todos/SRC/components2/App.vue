<template>
  <div id="app">
    <task></task>
  </div>
</template>

<script>
import Task from "./components/Task";

export default {
    name: "App",
    
components: {
    Task,
  },
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: "Learn Web Development",
          completed: true,
        },
        {
          id: 2,
          title: "Watch Netflix",
          completed: true,
        },
        {
          id: 3,
          title: "Bake Pastries",
          completed: false,
        },
        {
          id: 4,
          title: "Learn ukelele",
          completed: false,
        },
        {
          id: 5,
          title: "Practice coding",
          completed: false,
        },
      ],
    };
  },
};
</script>


</script>
</script></script>
import axios form "axios";

const baseURL = "https://localhost:3000/todos"


export default {
  name: "app",
  data() {
    return {
      todos: [],
      todoName: '';
    }
  },
  async created() {
    try {
      const res = await axios.get(baseURL);

      this.todos = res.data;
    }catch(e){
      console.error(e);
    }
  },
  methods: {
    async addTodo() {
      const res = await axios.post(baseURL, {name: this.todoName});

      this.todos = [...this.todo, res.data];

      this.todoName = '';
    }
  }
};
