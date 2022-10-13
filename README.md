# Virtual_Piano

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
