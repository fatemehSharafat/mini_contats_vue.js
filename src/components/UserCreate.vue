<template >
    <div class="component" >
        <div class="box1">
             <!-- input numder-->
            <input type="number" placeholder="شماره همراه" id="input1" v-model="pNumber" ref='pnum' defaultValue=''>
            <br><br>
            <div class="row justify-content-center">
                <!-- add user btn-->
                <div class="col-6">
                    <button type="button" class="btn  text-white" id="addper" @click="sendPnum()" >
                        <div class="row justify-content-center">
                            <div class="col-2"> 
                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-plus-fill" viewBox="0 0 16 16">
                                    <path d="M1 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H1zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"/>
                                    <path fill-rule="evenodd" d="M13.5 5a.5.5 0 0 1 .5.5V7h1.5a.5.5 0 0 1 0 1H14v1.5a.5.5 0 0 1-1 0V8h-1.5a.5.5 0 0 1 0-1H13V5.5a.5.5 0 0 1 .5-.5z"/>
                                </svg>
                            </div>
                            <div class="col-10">
                                افزودن همكار
                            </div>
                        </div>
                    </button>
                </div>
                <!-- phonebook btn-->
                <div class="col-6">
                     <button type="button" class="btn  text-white" id="phonbtn">
                        <div class="row justify-content-center">
                            <div class="col-2"> 
                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-lines-fill" viewBox="0 0 16 16">
                                    <path d="M6 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm-5 6s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H1zM11 3.5a.5.5 0 0 1 .5-.5h4a.5.5 0 0 1 0 1h-4a.5.5 0 0 1-.5-.5zm.5 2.5a.5.5 0 0 0 0 1h4a.5.5 0 0 0 0-1h-4zm2 3a.5.5 0 0 0 0 1h2a.5.5 0 0 0 0-1h-2zm0 3a.5.5 0 0 0 0 1h2a.5.5 0 0 0 0-1h-2z"/>
                                </svg>  
                            </div>
                            <div class="col-10">
                                دفترچه تلفن
                            </div>
                        </div>
                    </button>
                </div>

            </div>


        </div>

        
    </div>
</template>

<script>
export default {
   data() {
       return {
           pNumber:'',

           
       }
   }, 
   props:['items'],
   methods: {
       sendPnum(){
           if(this.pNumber.length >0 ){
               const pnum = this.pNumber;
               this.$emit('add-user' , pnum);
               return this.pNumber = ""
           }
       }
   },
}
</script>

<style>
 div.box1{
     background: white;
     padding: 20px;
     border-radius:19px ;
     box-shadow: 1px 1px 9px #eaeaea;
 }
#input1{
    border:none;
    background:rgb(249 249 249);
    width: 100%;
    border-radius:11px ;
    padding: 14px;
}
#addper{
    background-color: #8b4dd8;
    width: 100%;
    
}
#phonbtn{
    background-color: #308b39;
    width: 100%;
}
</style>