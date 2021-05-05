<template>
  <div>
    <section class="histeory_container">
      
      <div class="chat_header">
        <div class="chat_profile">
          <img src="@/assets/images/group.png" />
        </div>
        <div class="chat_title">
          <h1>Scarlet, Diana</h1>
        </div>
        <div class="total_members">
          <p>+5</p>
        </div>
        <div class="add_member">
          <div class="add_btn">
            <h1>+</h1>
          </div>

          <div class="icons"></div>
        </div>
        <div class="test"></div>
      </div>
      <div class="scroll_div">
        <!-- Sender Div satrt -->
        <div class="sender_info"> 
          <div class="chat_date">
            <p>Today</p>
          </div>
          <div class="sender_pic">
            <img src="@/assets/images/mud.jpg" />
          </div>
          <div class="sender_chat">

           
            <h2>Hi ! How are you?</h2>

            <div class="chat_time">
              <p>2:00 AM</p>
            </div>
            <!-- <img src="@/assets/images/mud.jpg" style="width:250px"/>
            <h2>I had an accident.</h2>
            

            <div class="chat_time">
              <p>2:30pm</p>
            </div> -->
          </div>
        </div>
        <!-- Sender Div end up-->

        <div class="reciver_info">
          <!-- Reciver Div Start -->
          <div class="reciver_chat">
            <h1>I am good? what about you?</h1>
            
          </div>
        </div>
        <!-- Reciver Div end up -->

        <!-- Sender Div satrt -->
        <div class="sender_info"> 
          <!-- <div class="chat_date">
            <p>Today</p>
          </div> -->
          <div class="sender_pic">
            <img src="@/assets/images/mud.jpg" />
          </div>
          <div class="sender_chat">

           
            <h2>Hi ! How are you?</h2>

            <div class="chat_time">
              <p>2:00 AM</p>
            </div>
            <img src="@/assets/images/chat_img.png" style="width:250px"/>
            <h2>I had an accident.</h2>

            <div  class="typind_div">
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            </div>
            <!-- <div class="chat_time">
              <p>2:00 AM</p>
            </div> -->
          </div>
        </div>
        <!-- Sender Div end up-->
            <div class="sender_info"> 
          <div class="chat_date">
            <p>Bruce Joined</p>
          </div>
          <div class="sender_pic">
            <img src="@/assets/images/Ahmed.jpg" />
          </div>
          <div class="sender_chat">

           
            <h2>Are you alright? </h2>
            <h2>You must take a day off.</h2>

            <div class="chat_time">
              <p>2:01 AM</p>
            </div>
            <!-- <img src="@/assets/images/mud.jpg" style="width:250px"/>
            <h2>I had an accident.</h2>
            

            <div class="chat_time">
              <p>2:30pm</p>
            </div> -->
          </div>
        </div>
        <!-- Sender Div end up-->
      </div>
      <div class="footer_area">
        <div class="chat-footer">
        
            <textarea class="form-control" type="textarea" placeholder="Type Message here..."  >
            </textarea>
          <!-- <button class="send_btn"> -->
              <div class="send_btn">
              <img src="@/assets/images/send_btn.png" />
              </div>
            <!-- </button> -->
            <div class="attachment_div">
            <img src="@/assets/images/clip.png" />
            </div>
           
            
         
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import mud from "@/assets/images/mud.jpg";
import ahmed from "@/assets/images/Ahmed.jpg";
export default {
  name: "ChatArea",
  data() {
    return {
      user_data: [],
    };
  },
};
</script>
<style scoped>
.histeory_container {
  width: 65%;
  height: 600px;
  /* border: 1px solid black; */
   margin-top: 22px;
  margin-left: 0px;

  float: left;
}
.chat_header {
  width: 100%;
  height: 60px;
  border-bottom: 1px solid #c3c3c3;
  /* border: 1px solid black; */
  
}
.chat_profile {
 width: 45px;
  height: 45px;
  padding: 3px;
  /* border:1px solid black; */
  float: left;
  
  margin-top:10px
  
}
.chat_profile img {
 width: 100%;
  border-radius: 50px;
  border:1px solid #c3c3c3;
  
}
.chat_title {
  height: 50px;
  width: auto;
  /* border:1px solid black; */
  float: left;
  margin-left: 5px;
  margin-top:10px
}
.chat_title h1 {
 margin-top:10px;
  font-family: sans-serif;
  font-size: 18px;
  color: #000000D9;
  font-weight: 300;
}

.total_members {
  height: 50px;
  width: 35px;
  /* border:1px solid black; */
  float: left;
  margin-left: 5px;
  margin-top:12px
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
  margin-top: 10px;
  border: 1px solid #c3c3c3;;
  font-weight: bold;
  font-family: sans-serif;
}
.add_member {
  height: 40px;
  width: 80px;
  /* border:1px solid black; */
  float: right;
  margin-top:10px;
  text-align: center;
}
.add_btn {
  float: left;
  height: 40px;
  width: 40px;
  border-radius: 50px;
  border: 1px solid black;
  text-align: center;
  padding: auto;
}
.icons {
  float: right;
  height: 40px;
  width: 20px;
}
.icons:before {
  content: "\2807";
  font-size: 25px;
}
.sender_info {
  clear: both;
  height: auto;
  width: 100%;
  /* border: 1px solid black; */
}
.chat_date {
  width: 100%;
  height: 20px;
  text-align: center;
  border: none;
}
.chat_date p {
  display: block;
  margin: auto;
  background-color: white;
  font-size: 12px;
  width: 80px;
  margin-top: 2px;
  padding: 0px;
  border-radius: 20px;
 border:1px solid #c3c3c3;
 color: #c3c3c3;
}
.sender_pic {
  height: 45px;
  width: 45px;
  padding:5px;
  /* border: 1px solid black; */
  float: left;
}
.sender_pic img {
  width: 100%;
  border-radius: 50%;
  border:1px solid #c3c3c3;
}
.sender_chat {
  float: left;
  width: 300px;
  height: auto;
  margin-top: 10px;
  /* border: 1px solid black; */
  display: flex;
  flex-flow: column;
  margin-left: 5px;
}
.sender_chat h2 {
  
  background-color:#f5f5f0;
  padding: 3px;
  border-radius: 5px ;
  padding-bottom: 0px;
  margin-left: 0px;
  font-size: 16px;
  font-weight: 600;
  width: 250px;
  /* border: 1px solid black; */
  margin: 0px;
  margin-top: 4px;
  color:black;
  opacity: 100%;
}
.chat_time {
  margin-top: 0px;
  font-size: 11px;
  width: 250px;
  text-align: right;
  /* border: 1px solid black; */
  background-color: white;
  color:#3f3e3e; ;
   margin: 0px;
   height: 20px;
   font-weight: 600;
  
  
}
.reciver_info {
  clear: both;
  width: 100%;
  height: auto;
  /* border: 1px solid black; */
}
.reciver_chat {
  float: right;
  width: 300px;
  height: auto;
  /* border: 1px solid black; */
  text-align: right;
  
}
.reciver_info h1 {
 
  background-color:#f5f5f0;;
  padding: 3px;
  font-size: 16px;
  font-weight: 600;
  width: 250px;
  border-radius: 5px ;
  float: right;
  padding-right: 20px;
  
}
.scroll_div {
  height: 400px;
  width: 100%;
  overflow-y: auto;
  scrollbar-width: none;
}
.footer_area {
  clear: both;
  width: 100%;
  margin-top: 20px;
  height: 80px;
  /* border: 1px solid black; */
  margin-bottom: 0px;
}
.chat-footer {
  
  padding: 0px;
  height: 100%;
  bottom: 0;
  width: 100%;
  /* border: 1px solid black; */
}
.form-control{
  width: 90%;
  float: left;
  height: 100%;
  background-color: #ebebe0;

}
.send_btn{
  float: left;
  margin-left: 10px;
  /* border: 1px solid black; */
  /* border-top-right-radius: 30px;
  border-bottom-right-radius: 30px; */
 
  width: 40px;
  height: 40px;
  color: white;
  margin-left: 3px;

}
.send_btn img{
  width:100%;
  background-color: white;
  /* transform: rotate(45deg); */
  
  opacity: 100%;
  
  cursor: pointer;
}
textarea{
  color:black;
  font-size: 20px;
  border: none;
  outline: none;
  border-radius: 5px;
  padding-left: 10px;
  height: 80px;
  
}
textarea::placeholder{
  color:black
}
.sender_chat span {
    display: inline-block;
    width: 180px;
    white-space: nowrap;
    overflow: hidden !important;
    text-overflow: ellipsis;
}
.typind_div{
  
  text-align: left;
  width: 250px;
  height: 30px;
}
.dot {
  
  height: 7px;
    width: 7px !important;
    background-color:#333399;
    border-radius: 50% !important;
}
.attachment_div{
  float: left;
  width: 20px;
  height: 20px;
  margin-top: 3px;
   transform: translate(-68px);
   cursor: pointer;
}
.attachment_div img{
   width: 20px;
   height: 20px;
  
}
/* ::placeholder */
</style>