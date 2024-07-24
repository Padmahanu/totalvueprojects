<template>
    <div>
<h2>fullname: {{first}} {{last}}</h2>
<h2>Computed full name : {{fullname}}</h2>
<button @click="changeFullName()">Change fullname</button><br/>
<button @click="items.push({id:4,price:3000 })">Add item</button>
<h2> Total -{{total}}</h2>
<h2>Get Total ={{gettotal()}}</h2>
<input type="text"  v-model="country">
 
    <template v-for='(item,i) in items' :key="item.id">
       <h2 v-if="item.price>100">{{item.id}} {{item.price}}</h2>
    </template>
       </div>
</template>

<script>
    export default {
        name:'App',
        data(){
            return {
                first: 'Padma',
                last: 'Hanu',
                items:[
                                            {
                        id:1,
                        price: 100
                                            },
                                            {
                        id:2,
                        price: 1000
                                            },
                                            {
                        id:3,
                        price: 2000
                                            }
                ],
                country:''
            }
        },
        computed:{
            fullname:{
get(){
return `${this.first} ${this.last}`
},
set(values){
const names=values.split(' ')
this.first=names[0];
this.last=names[1];
}
            },
// fullname(){
//     return `${this.first} ${this.last}`
// },
total(){
    console.log("total")
    return this.items.reduce((total,acc) => (total= total + acc.price),0);
}
        },
        methods:{
            changeFullName(){
                this.fullname ="Nudurpati Kannaya"
            },
gettotal(){
    console.log("get total")
    return this.items.reduce((total,acc) => (total= total + acc.price),0);
}
        }
    }
</script>

<style lang="scss" scoped>

</style>