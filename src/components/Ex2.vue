<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                newItem: ""
            }
            
        },
        methods: {
            add() {
                this.items.push(this.newItem)
            }

        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul v-for="(item, indx) in items">
        <li>{{ item }} <span><button @click="items.splice(indx, 1)">Delete!</button></span></li>
    </ul>
    <input type="text" v-model="newItem"></input>
    <button @click="add">Add!</button>
   
</template>
