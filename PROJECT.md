#

##
- 作业核心是做网络编程
## build 
- netimg 客户端，支持opengl显示
- imagdb 服务端，支持图像发送

```
 zhangbin@pb6a80114  ~/tet/licodelllcode/eecs489lab1/src   master  make
g++ -g -Wall -Wno-deprecated  -c netimg.cpp
g++ -g -Wall -Wno-deprecated  -c netimglut.cpp
g++ -g -Wall -Wno-deprecated -o netimg netimg.o netimglut.o -framework OpenGL -framework GLUT -lc
g++ -g -Wall -Wno-deprecated  -c imgdb.cpp
g++ -g -Wall -Wno-deprecated  -c ltga.cpp
g++ -g -Wall -Wno-deprecated -o imgdb imgdb.o ltga.o
```

## run
- server imgdb
```
 ✘ zhangbin@pb6a80114  ~/tet/licodelllcode/eecs489lab1/src   master ●  ./imgdb
imgdb address is pb6a80114.nigtnt01.ap.so-net.ne.jp:54989
Connected from client localhost:55011
Image: 
     Type   = RGB (1)
     Width  = 864
     Height = 432
Pixel depth = 24
Alpha depth = 0
RL encoding = 0
imgdb_send: size 1119744, sent 22394
imgdb_send: size 1097350, sent 22394
imgdb_send: size 1074956, sent 22394
imgdb_send: size 1052562, sent 22394
imgdb_send: size 1030168, sent 22394
imgdb_send: size 1007774, sent 22394
imgdb_send: size 985380, sent 22394
imgdb_send: size 962986, sent 22394
imgdb_send: size 940592, sent 22394
imgdb_send: size 918198, sent 22394
imgdb_send: size 895804, sent 22394
imgdb_send: size 873410, sent 22394
imgdb_send: size 851016, sent 22394
imgdb_send: size 828622, sent 22394
imgdb_send: size 806228, sent 22394
imgdb_send: size 783834, sent 22394
imgdb_send: size 761440, sent 22394
imgdb_send: size 739046, sent 22394
imgdb_send: size 716652, sent 22394
imgdb_send: size 694258, sent 22394
imgdb_send: size 671864, sent 22394
imgdb_send: size 649470, sent 22394
imgdb_send: size 627076, sent 22394
imgdb_send: size 604682, sent 22394
imgdb_send: size 582288, sent 22394
imgdb_send: size 559894, sent 22394
imgdb_send: size 537500, sent 22394
imgdb_send: size 515106, sent 22394
imgdb_send: size 492712, sent 22394
imgdb_send: size 470318, sent 22394
imgdb_send: size 447924, sent 22394
imgdb_send: size 425530, sent 22394
imgdb_send: size 403136, sent 22394
imgdb_send: size 380742, sent 22394
imgdb_send: size 358348, sent 22394
imgdb_send: size 335954, sent 22394
imgdb_send: size 313560, sent 22394
imgdb_send: size 291166, sent 22394
imgdb_send: size 268772, sent 22394
imgdb_send: size 246378, sent 22394
imgdb_send: size 223984, sent 22394
imgdb_send: size 201590, sent 22394
imgdb_send: size 179196, sent 22394
imgdb_send: size 156802, sent 22394
imgdb_send: size 134408, sent 22394
imgdb_send: size 112014, sent 22394
imgdb_send: size 89620, sent 22394
imgdb_send: size 67226, sent 22394
imgdb_send: size 44832, sent 22394
imgdb_send: size 22438, sent 22394
imgdb_send: size 44, sent 44


```
- client netimg 
```
./netimg -s 127.0.0.1:54989 -q BlueMarble2004-08.tga

```
- 渐进的收到图片并一点点的显示出来