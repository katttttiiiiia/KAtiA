<!doctype html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Tp1</title>
		<style>
			.slider{
				position:relative;
				width:500px;
				height:250px;
				margin:auto;
				/*border:2px solid black;/**/
				overflow:hidden;
			}
			.img{
				position:absolute;
				height:100%;
				width:100%;
                margin:0;
                padding:0 ;
				border:none;
				background-position:center;
				background-size:cover;
                transition:all ease 2s;
			}
		</style>
	
        
    </head>
	<body>

        <script>
            var i = 1;
            var j = 2;
            
    		function anim(){
			var idiv = i;
			var idivv = j;
			i=i+2;
			j=j+2;
			if(i>11){
				i = 1;
				j=2;
			}
			
			var sld = document.getElementById("sld");
			var imgsld = document.getElementById("imgsld");
			
				
					var div1 = document.createElement("div");
					var div2 = document.createElement("div");
					div1.setAttribute("class", "img");
					div2.setAttribute("class", "img");
					div1.setAttribute("style", "border:2px solid black ;bottom:0px;background-image:url(files/imag/"+idiv+".jpg);width:49%;height:240px;left:0px;background-size:50%;background-position:center;background-repeat:no-repeat; ");
					div2.setAttribute("style", "border:2px solid black ;bottom:0px;background-image:url(files/imag/"+idivv+".jpg);width:49%;height:240px;right:0px;background-size:50%;background-position:center;background-repeat:no-repeat;");
					sld.appendChild(div1);
					sld.appendChild(div2);/**/
					//imgsld.setAttribute("style", "background-image:url(files/img/"+i+".jpg)");
					setTimeout(function(){
						div1.style.borderRadius = "500px";
						div2.style.borderRadius= "500px";
						setTimeout(function(){
							div1.remove();
							div2.remove();
						},2000);
					},2000);
                setTimeout(anim, 4000);}
		
</script>
        
        <div class="slider" id="sld">
	
			<div class="img" id="imgsld" ></div>
			</div>
	<script>
		anim();
	</script>
    </body>
    </html>
