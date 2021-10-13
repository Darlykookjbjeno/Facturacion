<template>
  <table class="table tablesorter" >
    <thead>
      <tr>
        <th>0000</th>
        <th>0000</th>
        <th>0000</th>
                <th>0000</th>
      </tr>
    
    </thead>
    <tbody>
      <tr>
        
          <td>
            00000
          </td>

          <td>
            00000
          </td>

          <td>
            00000
          </td>

          <td>
            00000
          </td>
       
      </tr>
    </tbody>
  </table>
</template>
<script>
 export default {
   name: 'base-table',
   props:{
     
     theadClasses:{
       type: String,
       default: ''
     },
  
    
     columns:{
       type: Array,
       default: ()=>[]
     }
   },
   methods: {
     hasValue(item, column) {
       return item[column.toLowerCase()] !== "undefined";
     },
     itemValue(item, column) {
       return item[column.toLowerCase()];
     }
   }
 }
</script>
<style>
</style>
