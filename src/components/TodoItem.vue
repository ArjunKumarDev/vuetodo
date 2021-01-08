<template>
   <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
      <p>
      <input type="checkbox" v-on:change="markComplete" />
      {{todo.title}}
      <button class="todo-del" @click="$emit('del-todo',todo.id)">X</button>
 
      </p>
           
    </div>
    

</template>
<script>
export default {
    name:"TodoItem",
    props:["todo"],
    methods:{
        markComplete(){
            this.todo.completed = !this.todo.completed
            }
        }
}
</script>

<style lang="scss">

   $color-grey-dark: #f4f4f4;
   $color-grey-light : #ccc;
   $color-red: #ff0000;
   $color-white : #fff;

  .todo {
      &-item {
          background: $color-grey-dark;
          padding: 10px;
          border-bottom: 1px $color-grey-light dotted;
     }

       &-del {
        background: $color-red;
        color: $color-white;
        border: none;
        padding: 5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
     }
  }

  .is-complete {
    text-decoration: line-through;
  }

</style>