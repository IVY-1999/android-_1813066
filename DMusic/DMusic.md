# Android APP DMusic CodeLab

## 一、开发环境
- ### 操作系统：Windows 10
- ### 开发工具：JDK 1.8、Android studio 4.2.1
- ### API 版本：Android API 30
>
## 二、DMusic 总体介绍

### DMusic 是一个音乐播放器，主要包含4个页面：主页面、全部音乐、播放历史以及菜单界面。下面是界面展示：

### 1. 主界面
![主界面](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/主界面1.jpg)

### 2. 全部音乐
![全部音乐](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/全部音乐1.jpg)

### 3. 播放历史
![播放历史](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/播放历史1.jpg)

### 4. 菜单界面
![菜单](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/菜单1.jpg)
>
>
## 三、实现思路

### 1. 创建 Song.java 定义获取歌曲的信息，并且设置 item_song.xml 以及 activity_music_list.xml 文件：
#### (1) Song.java:
![Song.java](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/1.png)
>
#### (2) item_song.xml:
![item_song.xml](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/4.png)
>
#### (3) activity_music_list.xml:
![activity_music_list.xml](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/11.png)

### 2. 创建 Sheet.java , MusicListSheet.java 定义歌单，并且设置 item_sheet.xml 文件：
#### (1) Sheet.java:
![Sheet.java](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/6.png)
>
#### (2) MusicListSheet.java:
![MusicListSheet.java](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/10.png)
>
#### (2) item_sheet.xml:
![Sheet.java](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/5.png)
>
### 3. 创建 SheetAdd.java 实现添加歌单的功能，并设置 activity_add.xml 文件：
#### (1) SheetAdd.java:
![SheetAdd.java](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/8.png)
![SheetAdd.java](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/9.png)
>
#### (2) activity_add.xml:
![activity_add.java](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/7.png)
>
### 4. 创建 MusicUtils 实现从本地扫描音乐，并返回一个 list 集合：
![MusicUtils](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/2.png)
![MusicUtils](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/3.png)
>
### 5. 创建 MusicService.java 实现音乐的播放：
![MusicService](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/12.png)
>
### 6. 创建SheetAdapter.java 实现歌单适配：
![SheetAdapter](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/13.png)
>
### 7. 创建 Frag_introduction.java 实现 APP 主要功能的介绍，并设置 menu_introduction.xml：
#### (1) Frag_introduction.java:
![Frag_introduction.java](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/14.png)
>
#### (2) menu_introduction.xml:
![menu_introduction.xml]](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/15.png)
>
### 8. MainActivity.java、activity_main.xml:
#### (1) MainActivity.java: 见源代码
>
#### (2) activity_main.xml:
![activity_main.xml](https://github.com/IVY-1999/android_1813066/blob/main/DMusic/images/16.png)
