# moodle
moodle_ideo
1. 音频上传部分添加方式：
1.1 复制js文件到src/main/webapp/js

1.2 在src/main/webapp/video.jsp里面添加：
        <script src="/moodlevideo/js/recorder.js"></script>
        <script src="/moodlevideo/js/audio.js"></script>
        <script src="/moodlevideo/js/wav2mp3.js"></script>

1.3 以及body部分的最后加上：
 <pre id="log"></pre>

2. 配置方式
2.1 更改上传文件格式（从wav变为mp3）
如果要提交mp3格式的话：把audio.js里的saveFile函数里的send(blob)注释掉，然后去掉wav2mp3(blob, send(blob))的注释

如果更改为mp3格式，需要更改后端php代码的话请联系wechat: NanxiongHuang

2.2 更改上传地址
如果要更改上传的地址的话，更改audio.js里的send函数里的POST地址即可
目前上传到http://101.201.68.238/soundRecord/demo/file_upload/upload1.php
想查看上传效果可以访问http://101.201.68.238/soundRecord/demo/file_upload/test.wav

3. 上传方式
完成更改后，将整个项目传到git上

git账号：
xwasp1995@163.com
密码：
Dashuju2018

具体方法：
cd到moodlevideo目录，运行以下命令：
git init
git add -A
git commit -m "first commit"
git remote add origin git@github.com:xwasp1995/moodlevideo.git
git push -u origin master
