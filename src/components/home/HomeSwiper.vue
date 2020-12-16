<template>
    <div id="div1">
       <ul>
           <li>{{getDate}}</li>
           <li>{{getDate}}</li>
       </ul>
    </div>
</template>

<script>
import {formatDate} from '../../common/utils'

export default {
   name: 'HomeSwiper',
   computed: {
     getDate(){
       const date = new Date()
       return formatDate(date,'yyyy-MM-dd hh:mm:ss')
     }
   },
   mounted(){
      var oDiv = document.getElementById('div1')
      var oUl = oDiv.getElementsByTagName('ul')[0]
      var oLi = oUl.getElementsByTagName('li')
      oUl.innerHTML = oUl.innerHTML + oUl.innerHTML
      oUl.style.width = oLi[0].offsetWidth * oLi.length+'px'
      setInterval(() => {
            if(oUl.offsetLeft<-oUl.offsetWidth/2){
                    oUl.style.left = '0'
            }
            oUl.style.left = oUl.offsetLeft-3+'px'
         },150)
   }

}
</script>

<style scoped>
   #div1 {
    position: relative;
    width: 200px;
    height: 48px;
    overflow: hidden;
} 

 #div1 ul {
    position: absolute;
    width: 400px;
}
        
#div1 ul li {
    float: left;
    width: 200px;
    list-style: none;
} 
</style>