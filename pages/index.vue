<template>
<div class="container shadow-lg p-3 mb-5 bg-white rounded">
  <div class="row">
    <div class="col-6">
      <h3>Serial Number</h3>
      <input type="text" v-model="inputserialNumber" class="form-control" placeholder="Contoh. ALF.XXXXXXXXXXX">
    </div>
    <div class="col-6">
      <h3>Tipe Jenis Mesin</h3>
      <select v-model="jenisPrinter" class="form-select" style="width:100%;">
        <option selected>Pilih Jenis Print</option>
        <option value="1">Riecat Alfa Gen 1</option>
        <option value="2">Riecat Alfa Gen 2</option>
        <option value="3">Riecat Alfa Gen 3</option>
      </select>
      <small>Jika sesuai maka sistem otomatis mendeteksi sistem anda</small>
    </div>
  </div>
  <div class="row">
    <div class="col-6">
      <h3>E-mail</h3>
      <input type="text" v-model="inputEmail"  class="form-control" @input="cekInput()" placeholder="Masukkan Email Anda">
    </div>
    <div v-if="jenisPrinter == '2'" class="col-6 pt-3 mt-4">
      <button type="button" class="btn btn-primary btn-block rounded-pill">Cek Sekarang !</button>
    </div>
    <div v-else class="col-6 pt-3 mt-4">
      <button type="button" disabled class="btn btn-primary btn-block rounded-pill">Cek Sekarang !</button>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data(){
    return{
      serialNumber:'ALFX-55555',
      inputserialNumber:'',
      email:'admin@localhost.com',
      inputEmail:'',
      jenisPrinter:'',
    }
  },
  methods:{
    cekInput(){
      if(this.serialNumber == this.inputserialNumber && this.email == this.inputEmail){
        console.log("okay!")
        this.jenisPrinter='2'
      } else {
        this.jenisPrinter=''
      }
    }
  }
}
</script>
