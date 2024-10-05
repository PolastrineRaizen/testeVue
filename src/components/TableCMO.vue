<template>
    <div class="tableContainer">
      <table>
        <thead>
          <tr>
            <th class="text">#</th>
            <th class="text">Data</th> <!-- Coluna Data sempre presente -->
            <th v-for="(coluna, index) in colunas" :key="index">{{ coluna }}</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(item, index) in dados" :key="index">
            <td class="roxo-escuro">{{ index + 1 }}</td>
            <td class="selectable">{{ item.Data || 'N/A' }}</td>
            <td v-for="(coluna, colIndex) in colunas" :key="colIndex" class="roxo-claro">
              {{ item[coluna] }}
            </td>
          </tr>
        </tbody>
      </table>
    </div>
</template>
  


<script>
    export default {
        props: {
            colunas: Array,
            data: Array,
            dados: Array
        }
    };

    // style:
    import '../css/TableCMO.css'
</script>
  

