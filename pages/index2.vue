<template>
<div class="container">
    <div class="row d-flex justify-content-center">
        <table class="table">
        <thead>
          <tr>
            <th scope="col">Nama Sparepart</th>
            <th scope="col">Tanggal</th>
            <th scope="col">Teknisi</th>
            <th scope="col">Jumlah</th>
            <th scope="col">Status</th>
          </tr>
        </thead>
        <tr>
            <td>Capping Station L1800/1390</td>
            <td>21/04/2021</td>
            <td>BP Surabaya</td>
            <td>12</td>
            <td>Proses</td>
        </tr>
        <tr>
            <td>Capping Station L1800/1390</td>
            <td>20/04/2021</td>
            <td>BP Jember</td>
            <td>100</td>
            <td>Selesai</td>
        </tr>
        <tr>
            <td>Baut Epson L1800</td>
            <td>19/04/2021</td>
            <td>BP Malang</td>
            <td>20</td>
            <td>Selesai</td>
        </tr>
        <tr>
            <td>Baut Epson L1800</td>
            <td>18/04/2021</td>
            <td>BP Makasar</td>
            <td>5</td>
            <td>Selesai</td>
        </tr>
        </table>
    </div>
    <h3 class="text-center"> Grafik Jumlah Sparepart Berdasarkan dari hitungan hari.</h3>
     <client-only>
        <div>
            <VueApexCharts
                ref="realtimeChart"
                width="100%"
                type="line"
                :options="chartOptions"
                :series="series"
            ></VueApexCharts>
        </div>
  </client-only>
</div>
</template>
<script>
export default {
    components: {
        VueApexCharts: () => import('vue-apexcharts')
    },
    data() {
      return {
        chartOptions: {
          chart: {
            id: 'vuechart-example'
          },
          xaxis: {
            categories: ['21/04/2021','20/04/2021','19/04/2021','18/04/2021']
          }
        },
        series: [{
          name: 'Jumlah Sparepart mesin',
          data: [12,100,20,8]
        }]
      }
    },
};
</script>
