<template>
    <li>
        <label>
            <!--      这里勾选和取消勾选可以使用change和click作为事件处理-->
            <input type="checkbox" :checked="todo.complated">
            <span>{{todo.title}}</span>
        </label>
        <button class="btn btn-danger">删除</button>
    </li>
</template>


<script>
export default {
    name: "TodoItems",
    props:["todo","checkTodo"],
    methods:{
        checkon(e){
           this.checkTodo(e)
        }
    }
}
</script>

<style scoped>
/*item*/
li {
    list-style: none;
    height: 36px;
    line-height: 36px;
    padding: 0 5px;
    border-bottom: 1px solid #ddd;
}

li label {
    float: left;
    cursor: pointer;
}

li label li input {
    vertical-align: middle;
    margin-right: 6px;
    position: relative;
    top: -1px;
}

li button {
    float: right;
    display: none;
    margin-top: 3px;
}

li:before {
    content: initial;
}

li:last-child {
    border-bottom: none;
}

li:hover {
    background: #ddd;
}

li:hover button {
    display: block;
}
</style>