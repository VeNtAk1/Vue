<script>
export default {
    data() {
        return {
            hrefs: [
                {href: '1.html', text: 'text1'},
                {href: '2.html', text: 'text2'},
                {href: '3.html', text: 'text3'},
		    ],
            products: [
                {name: 'product1', price: 100, quantity: 5},
                {name: 'product2',price: 200,  quantity: 4},
                {name: 'product3',price: 300,  quantity: 3},
		    ]
        }
    },
    methods:{
       
    }
}
</script>


<template>
    <ul>
        <li v-for="elem in hrefs">
            <a href=elem.href>{{elem.text}}</a>
        </li>
    </ul>

    <table>
        <tr v-for="elem in products">
            <td>{{ elem.name }}</td>
            <td>{{ elem.price }}</td>
            <td>{{ elem.quantity }}</td>
        </tr>
    </table>

</template>
