# dentifying-code
验证码基础

<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
	<title>Document</title>
	<script type="text/javascript">
	window.onload=function(){
	    var send=document.getElementById('send'),
	        times=60,
	        timer=null;
	        
	    send.onclick=function(){
	      // 计时开始 
	    times=60;
	    clearInterval(timer);
        timer=setInterval(function(){
            times=times-1;
            send.value=times+"秒后重试";
            send.disabled=true;
            if(times<=0){
                clearInterval;
            
             send.value="发送验证码";
             send.disabled=false;
            
            }
           },1000)
	    } 
	}
	</script>
</head>
<body>
	<input type="button" id="send" value="发送验证码">
</body>
</html>
