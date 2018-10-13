                           Construct 2的新手指南
一、开始
   现在你设置,启动Construct 2。点击文件按钮,选择New。
   https://www.scirra.com/images/articles/filenew.png
   出现一个对话框，选择new empty project。
   https://www.scirra.com/images/articles/newprojdialog65.png
   点击右下角的open按钮,创建一个新的layout。
二、插入对象
   1.插入背景
   https://www.scirra.com/images/articles/bg.png
   双击layout中的某个空间来插入一个新的对象。一旦弹出新对象对话框,双击Tiled Background插入它。
   https://www.scirra.com/images/articles/insertobject.png
   会出现一个十字表示物体的位置。点击layout中的某个空间。编辑器打开时,点击Load an image from file 。
   让我们导入之前保存的瓷砖图像。点击文件夹图标从磁盘加载纹理,找到你下载的文件,并选择它。
   https://www.scirra.com/images/articles/loadtexturefromfile.png
   关掉编辑器。将Tiled Background对象的position调到“0，0”，size调到“1280，1024”（即layout的size）。
   https://www.scirra.com/images/articles/tiledproperties.png
   按Ctrl并且滚动鼠标滚轮放大或缩小。或者,单击view-Zoom out缩小几倍。
   https://www.scirra.com/images/articles/tiledui.jpg
   按下ctrl + 0或单击view-Zoom out to 100%回到1:1视图。
　 单击右边的layers。
   https://www.scirra.com/images/articles/layerstab.png
   你应该在列表中看到layer0。点击铅笔图标,将它重命名为background。现在单击绿色“添加”图标添加一个新layer，
　 将它命名为main如果你点击旁边的小挂锁图标背景,它将成为锁着的。你可以将background上锁，将main打开。
   https://www.scirra.com/images/articles/layersbar.png
   确保选中main。
   2.添加输入对象
   把你的注意力放回到layout,双击layout中的某个空间来插入一个新的对象。一旦弹出新对象对话框,选择mouse对象。
   再次选择相同的keyboard对象。
　 3.插入游戏对象
   Player：https://www.scirra.com/images/articles/player.png
   Monster：https://www.scirra.com/images/articles/monster.png
   Bullet:https://www.scirra.com/images/articles/Bullet.png
   Explosion:https://www.scirra.com/images/articles/explode.png
   双击layout中的某个空间来插入一个新的对象。一旦弹出新对象对话框,双击Sprite插入它。
   会出现一个十字表示物体的位置。点击layout中的某个空间。编辑器打开时,点击Load an image from file 。
   让我们导入之前保存的游戏图像。点击文件夹图标从磁盘加载纹理,找到你下载的文件,并选择它。
   将子弹和爆炸图片移动到layout外的地方。并且，将各个游戏对象重命名，分别命名为Player、Monster、Bullet和
   Explosion。
   4.插入行为
   插入8 direction movement行为到Player。
   https://www.scirra.com/images/articles/openbehaviors.png
   https://www.scirra.com/images/articles/add8dir.png
   同理，插入Scroll To和Bound to layout行为到Player。
   https://www.scirra.com/images/articles/playerbehaviors_2.png
   现在可以试着运行一下游戏！
   https://www.scirra.com/images/articles/runbutton.png
   5.插入其他行为
   插入Bullet movement和Destroy outside layout行为到Bullet。
   插入Bullet movement行为到Monster。
   插入Fade行为到Explosion。
   运行游戏你会发现Monster移动地很快，此时可以将Monster的速度从400改到80。
   https://www.scirra.com/images/articles/bulletproperties.png
   另外可将Bullet的速度改为600，并将Explosion的褪色的Fade out time改为0.5(半秒)。
   6.插入更多的Monster
   按Ctrl点击Monster并用鼠标拖动它。插入七到八个monster。
   https://www.scirra.com/images/articles/severalghosts.png
三、活动
   点击Event sheet 1。
   https://www.scirra.com/images/articles/eventsheettab.png
   1.添加第一个event
   双击空白页面，弹出一个对话框，选择system。
   https://www.scirra.com/images/articles/newevent_2.png
   然后在弹出的新对话框中选择Every tick。
   https://www.scirra.com/images/articles/everytickcnd.png
   https://www.scirra.com/images/articles/everytickempty.png
   然后点击Add action选择Player。
   https://www.scirra.com/images/articles/addactiondlg.png
   然后选择Set angle toward position。
   https://www.scirra.com/images/articles/playersetanglepos.png
   然后在弹出的对话框内X行输入Mouse X，Y行输入Mouse Y。
   https://www.scirra.com/images/articles/setangleposparams.png
   如果出现一个Error说Mouse is not an object name，那么双击空白页面，弹出一个对话框，选择Mouse。
   最后得到的应该是这样的：
   https://www.scirra.com/images/articles/alwayslookatmouse.png
   2.添加游戏功能
   （1）使Player具有射击功能
   双击空白页面，弹出一个对话框，选择Mouse。
   然后在弹出的新对话框中选择On click。然后选择Left clicked。
   然后点击Add action选择Player。
   然后选择Spawn another object。选择Bullet对象。layer的数值是1，image point的数值是0。
   https://www.scirra.com/images/articles/spawnbullet1.png
   如果你此时运行游戏，你会注意到子弹是从Player的中间射出,而不是从Player的枪中射出。
   右击项目或对象栏中的Player，并选择Edit animations。
   https://www.scirra.com/images/articles/editanimations.png
   Player的图像编译器又一次出现，点击origin键，同时弹出一个对话框。
   https://www.scirra.com/images/articles/imagepointstool.png
   https://www.scirra.com/images/articles/imagepointsdlg.png
   我们想要添加另一个像点代表枪,所以单击添加按钮。会出现一个蓝色的点,这是我们的新形象：
   https://www.scirra.com/images/articles/placingimagepoint.p
   关闭图像编译器。双击我们之前添加过的Spawn another object，并且将Image point的数值改成1。
   https://www.scirra.com/images/articles/spawnbullet2.png
   （2）使子弹可以杀死Monster
   双击空白页面，弹出一个对话框，选择Bullet。
   然后在弹出的新对话框中选择On collision with another object。然后选择Monster。
   点击Add action选择Monster，并在弹出的对话框中选择destroy。
   点击Add action选择Bullet,然后选择Spawn another object。选择Explosion对象。layer的数值是1，image point的数值是0。
   点击Add action选择Bullet，并在弹出的对话框中选择destroy。
   （3）爆炸的效果
　　运行游戏,尝试射击一个Monster。哎呀,爆炸后面有一大块黑的。
   https://www.scirra.com/images/articles/explosionnoadditive.png
   左击项目或对象栏中的Explosion，将Blend mode改为Additive。现在运行这个游戏，它是这样的：
   https://www.scirra.com/images/articles/explosionadditive.png
   （4）使Monster更聪明一点
   双击空白页面，弹出一个对话框，选择system。
   然后在新弹出的对话框中选择On start of Layout。
   点击Add action选择Monster，并在弹出的对话框中选择Set angle，将角度选择或填写为random(360)。
   https://www.scirra.com/images/articles/ghostshooterevent4.png
   Monster离开后将永远漫步layout之外,再也不会出现。让我们保持它们在里面。我们要做的是:
   双击空白页面，弹出一个对话框，选择Monster。
   然后在新弹出的对话框中选择Is outside Layout。
   点击Add action选择Monster，并在弹出的对话框中选择Set angle toward position。对于X, 填写Player.X;对于Y,填写Player.Y。
   （5）Instance variables（实例变量）
   实例变量允许每个怪物存储自己的健康价值。左击项目或对象栏中的Monster,点击Edit variables中的Add/edit来编辑变量。
   https://www.scirra.com/images/articles/instvars.png
   点击加号添加一个新的实例变量，将health填入name项目,Number填入Type项目,并且将Initial value的数值改为5。
   https://www.scirra.com/images/articles/healthinstvar.png
   这时你得到的应该是这样的：
   https://www.scirra.com/images/articles/healthadded.png
   现在Monster就有五条命啦。
   （6）改变events
   切换回Event sheet。现在,我们可以摧毁怪物。
   找到这个事件Bullet - on collision with Monster，你会注意到我们已经有了一个destroy monster的活动。让我们用subtract 1 from health来代替它。
   右击destroy monster活动，选择replace，就像下面这样：
   https://www.scirra.com/images/articles/replaceaction.png
   选择Monster，然后在弹出的对话框中选择Subtract from，之后选择Instance variable "health",并且 给Value项目输入1。点击Done。
   https://www.scirra.com/images/articles/sub1fromhealth.png
   现在我们用子弹射击一次Monster，它便会损失一条命，之后我们要添加一个项目，让Monster死亡。
   双击空白页面，弹出一个对话框，选择Monster。
   然后在新弹出的对话框中选择Compare instance variable，之后在弹出的对话框中分别填入Health, Less or equal, 0。
   点击Add action，选择Monster。在弹出的对话框中选择Spawn another object，点击Explosion，将layer的值改为1。
   点击Add action，选择Monster。在弹出的对话框中选择Destroy。
   https://www.scirra.com/images/articles/monsternohealth.png
   （7）计分
   右击空白页面，弹出一个对话框，选择Add global variable。
   https://www.scirra.com/images/articles/addglobal.png
   弹出一个对话框，在name项目中输入Score，现在看起来应该是这样的：
   https://www.scirra.com/images/articles/addglobalscore.png
   现在global variable出现在Event sheet中。
   https://www.scirra.com/images/articles/globalscorevar.png
   现在我们让Player每杀死一个Monster就能获得一分。
   在"Monster: health less or equal 0"这个项目中，点击Add action，并且选择System，在其中选择Add to (在Global & local variables下面)，
   之后的对话框中分别输入Score, value 1。现在看起来应该是这样的：
   https://www.scirra.com/images/articles/scoreeevent.png
   （8）创建一个抬头显示器(HUD)
   添加一个新的layer，并且把它的名字改为HUD。把它的Parallax改为0, 0。
   双击layout中的某个空间来插入一个新的对象。一旦弹出新对象对话框,双击Text插入它。
   把它放在layout的左上角。如果它是黑色的,这将很难看到，所以在属性栏选择粗体,斜体,黄色,并且选择一个稍大的字体。现在看起来应该是这样的：
   https://www.scirra.com/images/articles/textinlayout.png
   回到Event sheet。在我们之前添加的Every tick事件中，点击Add action，选择Text。在弹出的对话框中选择Set text，在弹出的对话框中输入"Score: " & Score。
   （9）最后的操作
   首先，我们应该让怪物在被射击后生成，假设被射击后3秒生成。添加一个新事件：
   双击空白页面，弹出一个对话框，选择system。
   然后在新弹出的对话框中选择Every X seconds，然后输入3。
   点击Add action选择System，并在弹出的对话框中选择Create object，然后在弹出的对话框中输入layer 1, 1400 (对于X), random(1024) (对于Y)。
   最后，我们让Monster在触碰到Player时，Player死亡。
   双击空白页面，弹出一个对话框，选择Monster。
   然后在新弹出的对话框中选择On collision with another object，然后选择Player。
   点击Add action，选择Player。在弹出的对话框中选择Destroy。
现在，你就可以运行这个游戏啦。

  

