<template>
    <div id="oldCatalog" class="oldCatalog">

       <!-- <div class="catpic"> -->
        <img class="catpicmedia" src="@/assets/img/2022_Cat_Cover-img.png" alt="Old Calalog Placeholder">
       <!-- </div> -->
      
       <div class="oldcatcontent">
            <h2 style="color: var(--clr-blue-700)">{{ $t('old_cat_title')}}</h2>
            <p> {{$t('old_cat_description')}} </p>
            <Button :title="this.$t('old_cat_btn')" 
                    @click="downloadFile()"
                    bColor="--clr-pink-700" 
                    tColor="--clr-white"></Button>
                    <button @click="downloadFile()"></button>
          
       </div>

        
    </div>

</template>

<script>
    import Button from '@/components/Button.vue'
    import axios from 'axios'
    //import { text } from 'body-parser';

    export default {
        mounted() {
          this.downloadFile();
      },
  methods: {
    downloadFile() {
              axios({
                    url: 'pages/index-subviews/Systemvetardagen 2022 - Katalog.pdf', // File URL Goes Here
                    method: 'GET',
                    responseType: 'blob',
                }).then((res) => {
                     var FILE = window.URL.createObjectURL(new Blob([res.data]));
                     
                     var docUrl = document.createElement('x');
                     docUrl.href = FILE;
                     docUrl.setAttribute('download', 'file.pdf');
                     document.body.appendChild(docUrl);
                     docUrl.click();
                });
  }},
        name: 'oldCatalog',
    
    components: {
        Button
    },
    data() {
        return {
      // the i18n translation variable
      translation: this.$t('the_fair'),

      item: [{url: './Systemvetardagen 2022 - Katalog.pdf', label: 'Katalog 2022'}],
        }
    }}


</script>
    
<style>
    .oldCatalog {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 10% 5%;
        align-items: center;
        gap: 20px;
        
      
    }
    .catpicmedia {
        width:50%; 
        height: auto;
    }

    @media (min-width: 1024px) {
		 .oldCatalog {
            flex-direction: row;
            padding: 20%;
            padding-left: 7%;
            padding-right: 13%;
         }
         .oldcatcontent {
            padding-left: 5%;
        }
	  }


</style>
