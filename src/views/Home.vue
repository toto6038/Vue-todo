<template>
<v-container>
  <div class="home">
    <h1>Welcome</h1>
    <p class="caption">Hola</p>
    <!-- <v-btn plain rounded color="purple lighten-5--text">I'm a plain button</v-btn>
    <v-btn depressed color="indigo lighten-2">
      <v-icon left large>mdi-email</v-icon>
      email
    </v-btn>
    <v-btn color="indigo darken-1" fab>
      <v-icon>mdi-antenna</v-icon>
    </v-btn>
    <v-btn color="indigo darken-1" fab class="mx-2">
      <v-icon color="white">mdi-robot</v-icon>
    </v-btn>
    <br/> -->
    <v-text-field
      rounded
      v-model.trim="input"
      @keyup.enter="addTask"
      @click:append-outer="addTask"
      name="name"
      label="Task"
      id="id"
      placeholder="Neokent bad bad"
      clearable
      outlined
      append-outer-icon="mdi-pencil-plus"
    ></v-text-field>
    <v-list>
      <v-list-item  v-for="(item, index) in list" :key="item.title" dense rounded>
        <v-list-item-action>
          <v-checkbox v-model="item.done"></v-checkbox>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title v-text="item.title"></v-list-item-title>
        </v-list-item-content>
        <v-list-item-action>
          <v-btn icon @click="removeTodo(index)">
            <v-icon color="grey">mdi-delete</v-icon>
          </v-btn>
        </v-list-item-action>
      </v-list-item>
    </v-list>
  </div>

</v-container>
</template>

<script>
// @ is an alias to /src

export default {
  data () {
    return {
      input: '',
      idForTodo: 0,
      list: []
    }
  },
  methods: {
    addTask () {
      if (this.input) {
        this.list.push({
          id: this.idForTodo,
          title: this.input,
          done: false
        })
        this.input = ''
        this.idForTodo++
      }
    },
    removeTodo (index) {
      this.list.splice(index, 1)
    }
  }
}
</script>
