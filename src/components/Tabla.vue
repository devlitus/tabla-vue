<template>
  <div>
    <b-table-simple hover small caption-top responsive>
      <caption>Tabla plara calcular el total de la canal y contra canal</caption>
      <b-thead head-variant="dark">
        <b-tr>
          <b-th colspan="2">TOTAL</b-th>
          <b-th colspan="2" class="text-center">CANAL</b-th>
          <b-th colspan="2" class="text-center">CONTRA CANAL</b-th>
        </b-tr>
      </b-thead>
      <b-tbody>
        <b-tr>
          <b-td colspan="2" class="align-middle text-center">{{ resultTotal }}</b-td>
          <b-td colspan="2">
            <b-form-input v-model="canal" @blur="suma"></b-form-input>
          </b-td>
          <b-td colspan="3">
            <b-form-input v-model="ccanal" @blur="suma"></b-form-input>
          </b-td>
        </b-tr>
      </b-tbody>
    </b-table-simple>
  </div>
</template>
<script>
export default {
  name: 'TablaSimple',
  data() {
    return {
      canal: '',
      ccanal: '',
      total: 0
    }
  },
  methods: {
    suma() {
      if (this.canal !== '' && this.ccanal !== '') {
        return this.total = Number(this.canal) + Number(this.ccanal);
      }
      // this.total = 0;
    }
  },
  computed: {
    resultTotal() {
      return Number(this.canal) + Number(this.ccanal)
    }
  }
} 
</script>