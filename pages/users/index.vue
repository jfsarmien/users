<template>
<section class="sec">
   <div class="header">List of User</div>
   
  <article>
   <div class="nav"><div class="par">Sample Navigation</div></div>
    <div class="art">
        <User
         v-for="user in users"
         :key="user.id"
         :image="user.image"
         :name="user.name"
         :email="user.email"
         :id="user.id"
        />
     <!-- <div class="f-left">
        <div class="img" style="background-image:url('https://www.shareicon.net/data/256x256/2016/07/05/791214_man_512x512.png');">
        </div> 
        <div class="txt">Mr. Anonymous</div>
     </div>
     <div class="f-left">
        <div class="img" style="background-image:url('https://www.shareicon.net/data/256x256/2016/07/05/791217_people_512x512.png');">
        </div> 
        <div class="txt">Mr. Anonymous</div>
     </div>
     <div class="f-left">
        <div class="img" style="background-image:url('https://www.shareicon.net/data/256x256/2016/07/05/791224_man_512x512.png');">
        </div> 
        <div class="txt">Mr. Anonymous</div>
     </div>
     <div class="f-left">
        <div class="img" style="background-image:url('https://www.shareicon.net/data/256x256/2016/07/05/791218_man_512x512.png');">
        </div> 
        <div class="txt">Mr. Anonymous</div>
     </div> -->

    </div>
    
  </article>
   <div class="footer">Footer</div>
</section>
</template>

    <script>
        import User from '@/components/User'
          export default{
             components:{
                User
             },
             asyncData() {
                   return new Promise((resolve, reject) => {
                      setTimeout(() => {
                        resolve({
                          users:[
                          {
                                id:"1",
                                image: "https://www.shareicon.net/data/256x256/2016/07/05/791214_man_512x512.png",
                                name: "John Doe",
                                email:"jd@gmail.com"
                          },
                          {
                                id:"2",
                                image: "https://www.shareicon.net/data/256x256/2016/07/05/791214_man_512x512.png",
                                name: "Eric Bladesoe",
                                email:"eb@gmail.com"
                          },
                          {
                                id:"3",
                                image: "https://www.shareicon.net/data/256x256/2016/07/05/791214_man_512x512.png",
                                name: "Ryan Roach",
                                email:"rr@gmail.com"
                          }

                          ]
                        })
                      },1500)
                   })
             }
          }
    </script>

<style scoped>
.sec{
    box-sizing: border-box;
    height: 700px;
}
.header{
    background-color: #2980b9;
    padding: 20px;
    text-align: center;
    font-size: 35px;
    color: white;
}
article{
    display: -webkit-flex;
    display: flex;
    height:100%;
}
.nav{
   -webkit-flex: 1;
    -ms-flex: 1;
    flex: 0.5;
    background: #ecf0f1;
    padding: 15px; 
}
.nav .par{
    background: #3498db;
    color: white;
    padding:5%;
    
}
.art{
    -webkit-flex: 3;
    -ms-flex: 3;
    flex: 3;
    background-color: white;
    padding: 10px;
}
/*.f-left{
      float: left;
      width: 300px;
      background: #ecf0f1;
      margin-left: 5%;
      border: 1px solid #95afc0;
      height: 250px;
      margin-top: 1%;
      box-shadow: 0 2px 2px #aaa;
}
.f-left .img{
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
}
.f-left .txt{
    text-align: center;
}*/
.footer{
    background-color: #2980b9;
    padding: 10px;
    text-align: center;
    color: white;
}
</style>