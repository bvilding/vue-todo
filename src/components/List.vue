<template>
    <div>
        <div class="container" id="list">
            <h4>Vue ToDo</h4>
            <div id="add-item" class="material-icons btn-floating btn-large waves-effect red" @click="addItem(todo)"><i class="material-icons">add</i></div>
            <ul>
                <li id="todo-item" v-for="item in list">{{ item.name }} 
                    <i class="material-icons edit" @click="editItem(todo)">edit</i>
                    <i class="material-icons delete" @click="removeItem(todo)">delete</i>
                </li>
            </ul>
            <input id="input" type="text" v-model="todo">
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            todo: null,
            list: [
                {
                    name: 'Popcorn',
                    id: null,
                    state: null,
                },
                {
                    name: 'Milk',
                    id: null,
                    state: null,   
                },
                {
                    name: 'Bread',
                    id: null,
                    state: null,   
                },
            ]
        }
    },
    methods: {
        addItem(item){
           this.list.push(
               {
               name: this.todo,
               id: null,
               state: null,
               })
           console.log(this.list)
        },
        removeItem(item){
            this.list.pop({
            });
        },
        editItem(item){
            console.log(this.list);
        }
        
    },
    
}
</script>

<style lang="scss" scoped>
    #list{
        background-color:#f2f2f2;
        padding: 20px;
        position: relative;

        #add-item{
            position: absolute;
            bottom: 15px;
            right: 15px;
        }
            #todo-item{
                display: grid;
                grid-template-columns: repeat(6,1fr);
                grid-gap:10px;
                grid-auto-rows: minmax(100px, auto);
            
                .edit{
                    grid-column:5;
                }
                .edit:hover{
                    color: blue;
                }
                
                .delete{
                    grid-column:6;
                }
                .delete:hover{
                    color:red;
                }
            }
        
    }
    
</style>
