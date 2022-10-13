# Virtual_Piano

### 运行效果：

![image](https://allall02.baidupcs.com/file/9eb793c74t012f5f1ff131bc5d4e2993?bkt=en-864c1d195a8f2f410f9e4e7217bf1fc6898001a65a53b1129d38f4d8980cbc03ee657eaf9ee9d1cac10acec76f8d7145107f0a2c9937991d8b754bb9b3f88d3c&fid=1101884420624-250528-107551101168156&time=1665663769&sign=FDTAXUbGERLQlBHSKfWqi-DCb740ccc5511e5e8fedcff06b081203-wQWVRf%2B%2BKYlFZD%2BPxd%2FueYj6GFw%3D&to=80&size=3998481&sta_dx=3998481&sta_cs=0&sta_ft=png&sta_ct=0&sta_mt=0&fm2=MH%2CBaoding%2CAnywhere%2C%2C%E6%B9%96%E5%8D%97%2Cce&ctime=1665663691&mtime=1665663757&resv0=-1&resv1=0&resv2=rlim&resv3=5&resv4=3998481&vuk=1101884420624&iv=0&htype=&randtype=&tkbind_id=0&newver=1&newfm=1&secfm=1&flow_ver=3&pkey=en-712729d32e193c956ef65d59aa9039b6977b5878f02da2e17d73ed0fe4736c5149f3860a57965686d13abe47eec7af3009857a121aaf4cf3305a5e1275657320&sl=76480590&expires=8h&rt=pr&r=609019146&vbdid=3967370585&fin=%E6%97%A0%E6%A0%87%E9%A2%98.png&fn=%E6%97%A0%E6%A0%87%E9%A2%98.png&rtype=1&dp-logid=8935492386314281162&dp-callid=0.1&hps=1&tsl=80&csl=80&fsl=-1&csign=J1qOztoibsBdWI46lrNlO7X29BE%3D&so=0&ut=6&uter=4&serv=0&uc=2519269499&ti=05df9239daa40647a2c93b754ba4ef849dfdc87620d43ce1305a5e1275657320&hflag=30&from_type=1&adg=c_53a798ee008f696fab273f47c25f65d1&reqlabel=250528_f_0d379c25691f1db02fd2dff786ffd19a_-1_e575750a3c4aa01749b9e79faa454520&by=themis)

![image](2.png)

### 演示视频：

https://www.bilibili.com/video/BV1D8411x78X

### 主要功能：

1.连接midi键盘弹奏，实时显示瀑布流/五线谱，实时分析和弦，实时显示当前调性（按自然大调理解）

2.播放midi文件，实时显示瀑布流/五线谱（可自定义根音，对和弦做更准确的判断）

### 其他功能：

1.将自定义图片保存至backgrounds文件夹，运行时按G切换背景图片

2.按T选择开启/关闭背景前透明矩形（方便显示，默认五线谱模式开启，瀑布流模式关闭）

3.按D取消调性自动识别（离调和弦密集、特殊调式识别不准确时用）

4.按C/B手动切换调性，按U将调性设为Unsettled

5.按A重新开启调性自动识别

6.按M切换瀑布流/五线谱显示模式（仅midi键盘模式有效）

7.按P更改和弦显示位置或取消显示（仅瀑布流模式）

8.按Q退出

### 运行方式：

安装pygame, mido等相关库，执行virtual_piano.py；virtual_piano_exe中包含pyinstaller生成的可执行文件，可直接运行

### global_settings.ini中的相关设置：

set_root_from_file      仅midi播放模式可用，是否从已保存的midi文件读取根音（避免一些转位和弦的误识别）

background_folder_path  背景图片目录（无需修改文件名）

font_path               字体文件目录（更改字体可能会显示错位，需要在virtual_piano.py中修改相关位置参数）

midi_file_path          midi播放模式播放的midi文件（暂时只支持一个轨道）

root_file_path          当set_root_from_file = 1时，从指定midi文件读取根音

[WhiteKeyColor]         白色琴键按下时显示的颜色RGB值

[BlackKeyColor]         黑色琴键按下时显示的颜色RGB值

[WaterFallColor]        瀑布流外轮廓颜色RGB值

[WaterFallColor2]       瀑布流颜色RGB值

[WhiteKeyOnSustain]     白色琴键松开，踏板踩下时显示的颜色RGB值

[BlackKeyOnSustain]     黑色琴键松开，踏板踩下时显示的颜色RGB值

[ChordTextColor]        和弦字体颜色RGB值

[NoteListTextColor]     音符列表字体颜色RGB值

[SustainTextColor]      踏板状态字体颜色RGB值

[KeyTextColor]          调号字体颜色RGB值

[SpeedTextColor]        速度字体颜色RGB值

[TopSquareColor]        顶端矩形颜色RGB值

[TransScreenColor]      背景前透明矩形颜色RGB值

trans_screen_opacity    背景前透明矩形透明度

top_square_opacity      顶端矩形透明度

[GlobalResolution]      全局分辨率（默认1920x1200，更改分辨率为裁剪而非缩放，需要修改offset）

[BackGroundOffset]      背景图片位移值

piano_key_offset        钢琴键水平位移值

[MusicScoreOffset]      五线谱位移值

time_delta              midi播放速度

root_delta              当set_root_from_file = 1时，该值为待播放midi文件与根音midi文件时间差

### 存在问题：

1.部分和弦识别不准确，斜杠和弦/非三度叠置和弦/过于复杂的和弦难以识别

2.调性识别功能有待进一步增强，目前仅能在没有离调的情况下识别出自然大调

3.不支持低分辨率

4.存在一些不规范的记谱（非错误，不严谨但是不影响识谱）

5.midi仅支持单轨，不支持变速MIDI播放
