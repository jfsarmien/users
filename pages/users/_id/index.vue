<template>
  <section class="sec">
   <div class="header">User Profile</div>
   
  <article>
   <div class="nav"><div class="par"><nuxt-link id="bac" to="/users">List Of User</nuxt-link></div></div>
    <div class="art">
        <div class="f-container">
            <div class="f-left"> 
                 <div><img :src="users.image"></div>
                 <div style="text-align:center">{{ users.email}}</div>
            </div>
            <div class="f-left"> 
                 <div class="info">Username: {{users.username}}</div>
                 <div class="info">Name: {{users.name}}</div>
                 <div class="info">E-mail: {{users.email}}</div>
                 <div class="info">Address: {{users.address}}</div>
                 <div class="info">Company: {{users.company}}</div>
                  <div class="info">Website: {{users.website}}</div>
            </div>
        </div>

    </div>
    
  </article>
   <div class="footer">Footer</div>
</section>
</template>
<script>
        import User from '@/components/User'
          export default{
  
             asyncData(context) {
                   return new Promise((resolve, reject) => {
                      setTimeout(() => {
                        resolve({
                          users:[{
                                id:"1",
                                image:'https://www.shareicon.net/data/256x256/2016/07/05/791214_man_512x512.png',
                                name:"John Doe",
                                email:"jd@gmail.com",
                                address:"Bacong Negros Oriental",
                                username:"doej",
                                company:"Magnolia",
                                website:"www.magz.com"
                          },{
                                id:"2",
                                image: 'https://www.shareicon.net/data/256x256/2016/07/05/791214_man_512x512.png',
                                name: "Eric Baldesoe",
                                email:"eb@gmail.com",
                                address:"Sibulan Negros Oriental",
                                username:"ric",
                                company:"Chezzy One",
                                website:"www.1chez.com"
                          },
                          {
                                id:"3",
                                image: "https://www.shareicon.net/data/256x256/2016/07/05/791214_man_512x512.png",
                                name: "Ryan Roach",
                                email:"rr@gmail.com",
                                address:"Dauin Negros Oriental",
                                username:"ry",
                                company:"Last Resort",
                                website:"www.sort.com"
                          }].find(el => el.id === context.params.id)
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

.footer{
    background-color: #2980b9;
    padding: 10px;
    text-align: center;
    color: white;
}
.f-container{
    width: 100%;
    height: 400px;
}
.f-left{
      float: left;
      width: 300px;
      margin-left: 5%;
      height: 250px;
      margin-top: 1%;
}
.f-left .img{
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
}
.f-left .info{
    font-size: 20px;
}
#bac{
    text-decoration: none;
     text-align: center;
    color: white;
}
</style>