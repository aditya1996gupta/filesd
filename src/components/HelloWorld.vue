<template>
<div @submit.prevent="getData">
<employee />
 <input type="file" name="fileToUpload" id="fileToUpload">
  <input type="submit" value="process" name="submit" ><br />
  <textarea disabled style="overflow:auto;resize:none" rows="23" cols="50" v-model="message" />
</div>
</template>

<script>
import axios from 'axios'
export default {
  data(){
    return{
      data:{}
    }
  },
  methods: {
    async getName(){
      const { data } = await axios.get("https://{{}}/?name=michael");
      this.data = data;
    }
  }
}
</script>
