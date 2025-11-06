test
[testcamera.html](https://github.com/user-attachments/files/23385933/testcamera.html)
<!doctype html>
<title>摄像头+WebXR 自检</title>
<h2 id=m></h2>
<script>
m.innerText='① 是否 HTTPS：'+ (location.protocol==='https:' ? '✅' : '❌ 请用 https 打开');
navigator.mediaDevices?.getUserMedia({video:true})
  .then(()=>m.innerHTML+='<br>② 摄像头授权：✅')
  .catch(e=>m.innerHTML+='<br>② 摄像头授权：❌ '+e);
navigator.xr?.isSessionSupported('immersive-ar').then(y=>m.innerHTML+='<br>③ WebXR AR：'+(y?'✅':'❌'));
</script>
