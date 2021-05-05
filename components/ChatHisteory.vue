<template>
  <div>
    <section class="histeory_container">
      <h1
        style="
          margin-left: 4px;
          font-size: 18px;
          font-weight: 600;
          font-family: sans-serif;
          font-style: bold;
        "
      >
        Chat
      </h1>
      <div class="active_users">
         <!-- <input type="text" name="search" placeholder="Search.."> -->
        <input type="text" placeholder="Search..." v-bind:class="{active:class_status}" />
         <div class="icon" @mouseover="class_status = true"  >
          <span >&#9906;</span>
        </div>

        <!-- <div class="user_img" v-for="user in user_data" :key="user.id">
          <img :src="user.profile_pic" />
        </div> -->
      </div>
      <div class="scroll_div">
        <div class="chat_logs" v-for="user in user_data" :key="user.id" :style="[user.msg_count.length>=1 ? {'border-left': '5px solid #00cc00'} : {}]">
          <div class="profile_pic">
            <img :src="user.profile_pic" />
          </div>
          <div class="user_name">
            <h1>{{ user.name }}</h1>
          </div>
          <div  v-if="user.total_member.length>0">
          <div class="total_members">
          <p>+{{user.total_member}}</p>
        </div>
          </div>
        <div  v-else>
          <p></p>
        </div>
          <div class="msg_count">
            <p :style="[user.msg_count.length>=1 ? {} : {'background': 'none'}]"> {{ user.msg_count }}</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import mud from "@/assets/images/mud.jpg";
import ahmed from "@/assets/images/Ahmed.jpg";
import group from '@/assets/images/group.png'

export default {
  name: "ChatHisteory",
  data() {
    return {
      user_data: [
        { id: 1, profile_pic: mud, name: "Diana", msg_count: "1" ,total_member:''},
        { id: 2, profile_pic: ahmed, name: "Scarlet", msg_count: "999",total_member:'' },
        { id: 3, profile_pic: ahmed, name: "Brue Wayne", msg_count: "" ,total_member:''},
        { id: 4, profile_pic: ahmed, name: "Diana ", msg_count: "",total_member:'' },
        { id: 5, profile_pic: ahmed, name: "Scarlet", msg_count: "",total_member:'' },
        { id: 6, profile_pic: group, name: "Scarlet, Diana", msg_count: "999" ,total_member:'5'},
        { id: 7, profile_pic: group, name: "Scarlet, Diana", msg_count: "" ,total_member:''},
      ],
        class_status: false,
    };
  },
  
};
</script>
<style scoped>
.histeory_container {
  width: 30%;
  height: 600px;
  border-right: 1px solid #c3c3c3;
  float: left;
  margin-right: 15px;
  margin-top: 8px;
  padding-right: 15px;
}
.active_users {
  width: 100%;
  height: 40px;
  border-bottom: 1px solid #c3c3c3;
  display: flex;
  flex-flow: row wrap;
  margin-left: 10px;
  /* border: 1px solid black; */
}
input{
  height: 30px;
 
  font-size: 1.2em;
  outline: none;
  margin-left: 10px;
  width: 0%;
  border: none;
  border-bottom: 1px solid  #c3c3c3; ;
}
.icon{
  height:30px ;
  width: 15%;
  background-color: white;
  display: flex;
  justify-content: center;
  font-size: 1.8rem;
  color:black;
  cursor: pointer;
  transform: translate(-20px);

}
.icon span{
  margin-right: 20px;
   margin-bottom: 20px;
  transform: rotate(-45deg);
}
.active{
  width: 80%;
}

.user_img {
  width: 40px;
  height: 40px;
  padding: 5px;
}
.user_img img {
  width: 100%;
  border-radius: 50%;
}
.scroll_div {
  height: 500px;
  width: 100%;
  overflow-y: auto;
}
.chat_logs {
  margin-top: 5px;
  width: 100%;
  height: 45px;
  
  display: flex;
  flex-flow: row wrap;
  
}
.chat_logs:hover{
  background-color: #f5f5f0;
}
.profile_pic {
  width: 45px;
  height: 45px;
  padding: 5px;
  
}
.profile_pic img {
  width: 100%;
  border-radius: 50px;
  border:1px solid #c3c3c3;
  
}
.user_name{
  height: 45px;
  width: auto;
  float: left;
}
.user_name h1 {
  margin-top: 14px;
  margin-left: 3px;
  width:auto ;
  font-family:sans-serif;
  font-size: 18px;
  font-weight:300;
  color: black;
 
  
  
}
.msg_count {
  text-align: center;
  float: right;
  height: 100%;
  width: auto;
  margin-right: 0px;
  margin-left: auto;

      
  
  /* border: 1px solid black; */
}
.msg_count p {
  /* font-family: sans-serif;
  font-size: 12px;
  font-weight: 100;
  color: white;
  margin-top: 10px;
  margin-left: 10px;
  margin-right: 10px;
  background-color: #15b415;
  
  height: 25px;
  width: 25px;
 padding: 5px 10px;
  border-radius: 50%; */
    font-size:.8em;
   background:rgb(10, 172, 10);
   color:white;
   width:20px;
   height:18px;
   text-align:center;
   line-height:18px;
   border-radius:50%;
}

.total_members {
  height: 50px;
  width: 35px;
  /* border:1px solid black; */
  
  float: left;
  margin-left: 5px;
}
.total_members p {
  background-color: white;
  font-size: 13px;
  color:black;
  margin-left: 3px;
  padding-top: 0px;
  padding-left: 8px;
  font-size: 10px;
  padding-bottom: 0px;
  padding-right: 2px;
  border-radius: 50px;
  margin-top: 15px;
  border: 1px solid #c3c3c3;;
  font-weight: bold;
  font-family: sans-serif;
}

.badge {
    display: inline-block;
    min-width: 16px; /* pixel unit */
    padding: 35px 50px; /* pixel unit */
    border-radius: 50%;
    font-size: 75px;
    text-align: center;
    background: #1779ba;
    color: #fefefe;
}

</style>