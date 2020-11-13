<template>
  <v-container>
<!-- <v-btn @click="fetchData">
  Button
</v-btn> -->
  <!-- <v-simple-table dense>
    <template v-slot:default>
      <thead>
        <tr>
          <th width="200px" class="text-left">
            Наименование
          </th>
          <th  width="200px" class="text-left">
            Цена
          </th>
          <th  width="200px" class="text-left">
            Остаток
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in nameslist"
          :key="item[1].B[1].T"
        >
          <td>{{ item[1].B[1].N }}</td>
          <td>{{ item.calories }}</td>
          <td>{{ item.calories }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table> -->
  </v-container>
</template>

<script>
import data from '../data/data.json'
import names from '../data/names.json'
  export default {
    name: 'List',

    data () {
      return {
        dataList: data.Value.Goods,
        nameslist: names,
        arr: [1,2,3,4],
        arrayofBooks: [],
        desserts: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
        },
        {
          name: 'Eclair',
          calories: 262,
        },
        {
          name: 'Cupcake',
          calories: 305,
        },
        {
          name: 'Gingerbread',
          calories: 356,
        },
        {
          name: 'Jelly bean',
          calories: 375,
        },
        {
          name: 'Lollipop',
          calories: 392,
        },
        {
          name: 'Honeycomb',
          calories: 408,
        },
        {
          name: 'Donut',
          calories: 452,
        },
        {
          name: 'KitKat',
          calories: 518,
        },
      ],
      }
      },
    computed:{

    },
    methods: {
      fetchData(){
        console.log('this datalist',this.dataList);
        console.log('this nameslist',this.nameslist);
        // [1].B[1].N
        console.log('this arr',this.arr);
      },
    // booksData(){
    //   for (let i = 0; i < array.length; i++) {
    //     const element = array[i];
        
    //   }
    //   this.arrayofBooks = this.nameslist.map()
    // }
    }
  }
</script>
