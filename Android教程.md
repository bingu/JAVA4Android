# Android 教程

##	初级篇

### 一 JDK 安装

#### 1. 下载 Java 的开发包 JDK

JDK有好几个类型版本，我们只需要选择Java SE类型的版本就行了。
这里作为开发人员，我们选择JDK而不是JRE。
官方提供不同平台的版本可供下载，对于Windows平台，有32位和64位两种，根据自己电脑的Windows平台的版本进行相应选择。

下载网址:<http://www.oracle.com/technetwork/java/javase/downloads/index.html>
#### 2. 安装 JDK

自定义安装路径后，一路Next。

#### 3. 配置环境变量

+ path 环境变量，添加JDK中得 bin 文件夹路径。
+ classpash 环境变量，添加 “.”。

#### 4. 检查环境变量配置

CMD中输入：java -version，并回车。

如果返回 Java 版本信息，则配置成功.

如果不成功，通常是环境变量设置不正常，现在Windows平台的JDK都是做好的安装包，一般正常安装后都没有问题。

总结：到此为止，Windows平台的JDK就安装好了。

### 二 Eclipse 配置

#### 1. Eclipse 下载

在前面我们配置好了JDK环境后，就可以开始配置Android的集成开发环境了，官方Google推荐的集成开发环境为Eclipse，所以我们就以Eclipse作为集成开发环境。无论是在Linux平台上开发还是在Windows平台上开发，我们只需要下载相应平台的Eclipse版本就可以了。具体在Eclipse上的开发过程，都是相同的。Eclipse是一个开放的集成开发环境，所谓开放，是指其既是源代码开源（即Eclipse本身的源代码是开源的），又是指其具有良好的扩展性（既可以在Eclipse上开发插件也可以开发像Eclipse这样风格的应用程序）。

Eclipse的下载主页为：<http://www.eclipse.org/downloads/>

对于Android开发，我们下载Eclipse IDE for Java EE Developers版本，这个虽然是针对J2EE的开发版本，但插件比较全，也适合Android开发。每一个平台都对应32位和64位两种版本，根据自己电脑的操作系统情况选择相应的版本。

下载后的文件是zip压缩格式，Eclipse不是安装包的形式，直接解压缩后就可以运行了。前面我们已经讲了JDK的配置，如果按照前面讲的那样配置好JDK后，直接运行eclipse.exe程序就行了。

#### 2. 配置 Eclipse

在Eclipse中配置Android开发环境主要包括ADT(AndroidDevelopment Tools)和Android SDK两部分的安装。

在Eclipse的菜单中选择Help->Install New Software，鼠标点击右上方的“Add”按钮，在Location栏目中加入ADT的下载地址：https://dl-ssl.google.com/android/eclipse/，Location上边的 Name 栏目可以填写也可以不填写。然后点击“OK”按钮。

如果成功访问Google的相关服务器的话，会显示获取的ADT插件信息，鼠标选中里边的复选框。

一路Next就好，一旦下载安装成功会提示你重启Eclipse，点击“RestartNow”按钮重启Eclipse。

最新的Android SDK在 <http://developer.android.com/sdk/index.html> 下载。

SDK共支持三种平台Windows，Linux和Mac OS X。根据自己电脑的操作系统环境选择相应的版本。直接使用zip文件版本就行了。下载后把zip文件解压缩，放到自己喜欢的目录下。从Eclipse的菜单Window->Preferences中打开Preferences窗口，鼠标点击左边的Android，然后在右边点击“Browse”按钮设置Android SDK 的位置，就是前面下载的Android SDK解压缩后的位置。

最后点击右下方的“OK”按钮就行了。这样AndroidSDK就配置好了。

## Android 入门篇

### 一 创建第一个Android应用

#### 1. 创建一个Android Project

原文链接:<http://docs.eoeandroid.com/training/basics/firstapp/creating-project.html>

**创建Android项目**

一个安卓工程包含了组成android应用的所有源代码的文件。Android软件开发工具包(Software Development Kit，即SDK)可以让你轻松地创建一个包含了默认项目目录和文件的工程。
这一小节首先讲述的是怎么使用一个装有ADT插件的Eclipse创建一个新的工程，或者是在命令行下使用SDK工具创建新的工程。

>**注意：** 你应该已经安装了Android SDK，并且如果你使用的是Eclipse，你也应该安装了ADT插件。如果你没有安装这些工具，你应该查看安装Android SDK,当你完成安装后再返回到这里。

**使用Eclipse创建项目**

1.	在Eclipse中，选择File>New>Project。在弹出的对话框中应该有一个标有Android的文件夹（如果你没有发现Android的文件夹，那么你就是没有安装ADT插件，查看 安装ADT插件-Installing the ADT Plugin）。
2. 打开Android的文件夹，选择“Android Project”，然后点击“Next”。
3. 在“Application Name”矿中输入项目名称（比如“MyFirstApp”），然后点击“Next”。
4.	选择一个构建目标。被选中的版本将作为要编译你的应用的版本。

	我们建议你尽可能的选择最新版本。你仍然可以创建支持较旧版本的应用，但是选择最新版本的应用可以让你更加轻松的优化你的应用，以使得使用最新的android设备有更佳的用户体验.

5.	设置应用程序的其他细节，比如：

	Application Name:显示给用户看的应用程序名称，输入“My First App”。

	Package Name:你的应用程序的包的命名空间（请按照Java编程语言的规范来命名空间）。你的包名称必须和所有安装在Android系统中的应用程序的包名不相同。由于这个原因，使用一个适合您的公司或出版商标准的域风格的包名是十分重要的一点。

	Create Activity:这是你
的应用中基本的用户活动的类的名字（一个用户活动代表的是你的应用中的一个单独的画面。输入“MyFirstActivity”）。

	Minimum SDK：选择4（android1.6）

	因为这个版本较应用中选择的构建目标要低，会出现一个警告，但是这是可以的。在没有事先使用一些代码区确定设备的系统版本的情况下（你将会在其他的课程中学习到怎么做），你只需要确定你没有使用任何比minimum SDK的API线更高的API版本就可以。

6.	点击“Finish”。

到此，你的Android的项目现在已经建立起来了。这个项目中包含了一些默认的文件。你现在就可以去建造你的应用了。

#### 2. 运行你的程序

本节将教您：

+ 在真机上运行应用程序
+ 在虚拟机上运行应用程序

如果你跟随上一节创建了一个Android工程，那么它包含了一组默认的，直接就可以正确的运行的 “Hello World”源文件。

运行您的这个应用程序取决于两件事情：是否拥有一个真实的基于Android的设备并且是否使用Eclipse。这一节说明如何安装和运行应用程序在真实的设备或者是Andorid模拟器上，不论您是使用Eclipse还是命令行工具。

在你运行您的应用程序前，你应该认识一下Android工程中几个目录和文件。

+	AndroidManifest.xml

	这个manifest文件描述应用程序的基本属性，并且定义 应用程序中 的每一个组件。您今后学习更多的课程时将会学到其中更多的声明。

+	src/

	这个目录是您的源程序的主要目录。在默认情况下，目录包含一个Activity类，当您点击应用程序图标时就会运行它。

+	res/包含几个子目录，里面是应用程序的资源文件。下面是几个例子：
	
	drawable-hdpi/

	这里存放的是 为高分辨率（hdpi）屏幕所设计的 drawable objects（bitmaps图片）。其他的drawable目录包含为其他分辨率设计的资源（图片）。

	layout/

	这个目录的文件用来定义应用程序的用户界面。

	values/

	此目录包含其他各种资源集合的 XML文件 ，比如字符串、颜色的定义。

当您构建和运行默认的Android工程，在src目录中默认的Activity类就开始运行，并且从layout目录加载一个布局文件，这个布局文件包括一个“Hello World"信息。虽然没什么好激动的，但是这对您在实现真正功能的应用程序前，理解怎样构建和运行应用程序是非常重要的。

**在真机上运行应用程序**

不论您是使用Eclipse还是命令行工具，您需要：

1. 用USB线缆连接您的Android设备和电脑。如果您在Windows环境中开发，您需要为设备安装正确的USB驱动。需要得到安装驱动的帮助，请看文档《OEM USB驱动》。
2. 确保设备中的”USB调试“选项被打开（多数是在"设置"->"应用程序"->"开发"或者是在4.0以上系统中的"开发人员选项"中）。
从Eclipse中运行应用程序，打开一个您的工程文件，点击工具条中的Run。Eclipse会安装应用程序到您所连接的设备中并开始运行它。

**在模拟器上运行应用程序**

不论您使用Eclipse还是命令行工具，首先需要创建一个Android虚拟设备(AVD)，AVD是一个针对设备配置的Android模拟器，它允许你更改各种不同的设备配置。

创建一个AVD：

1.	打开Android虚拟设备管理器：

	在Eclipse中，选择 Window > AVD Manager,或者在工具栏上点击 AVD Manager 的图标。

2.	android avd在 Android Virtual Device Device Manager面板上点击"New".
3.	填写AVD详细信息，给它起个名字，选择目标平台，SD卡的容量和屏幕尺寸。
4.	点击 Create AVD。
5.	在 Android Virtual Device Manager 中选择新建的AVD，并且点击 Start。
6。	模拟器启动后，解锁模拟器的屏幕。

从Eclipse中运行应用程序，打开您的一个工程文件，并点击工具条上的Run。Eclipse 会安装应用程序到您的AVD并运行它。

#### 3. 构建一个简单的用户界面

Android的图形用户界面使用View和ViewGroup的层级类进行创建。View类是通用的UI窗体小部件，比如按钮或者文本框，而ViewGroup是用于定义子View布局的可视化容器，比如网格部件(grid)和垂直列表部件(list)。

Android提供了对应于View和ViewGroup子类的XML查询表，你可以在XML里使用层级视图元素创建自己的UI。

ViewGroup类在布局里形成的分支并且包含View类。

在这一次教程里，你将学到怎样用XML创建一个带有文本输入框和按钮的界面。在接下来的课里，你将学会对按钮做出响应，当按钮被按下的时候文本框里的内容被发送到另外一个Activity。

**使用线性布局**

从目录res/layout里打开main.xml文件(每一个新创建的Android项目都默认包含这个文件)。

>注意：在eclipse中，当你打开布局文件的时候，首先看到的是ADT布局编辑，这个编辑页是使用所见即所得的工具帮助你创建布局。对于本课来说，你是直接在XML里进行操作，因此点击屏幕下方的main.xml标签进入XML编辑页。

在默认的情况下，main.xml中包含一个线性布局和文本框。这里你可以重用线性布局，但是需要改变里面的内容和布局方向。结果如下：

	<?xml version="1.0" encoding="utf-8"?>
	<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
		android:layout_width="fill_parent"
		android:layout_height="fill_parent"
		android:orientation="horizontal" >
	</LinearLayout>

线性布局是ViewGroup的一个子类，用于放置水平或者垂直放置子视图的部件，由属性android：orientation来设定方向。线性布局里的子布局按照XML里设定的顺序显示在屏幕上。

另外的两个属性android：layout_width 和 android:layout_height，对于所有的部件都需要对这两个属性进行设置。

在这里因为线性布局是整个视图的根布局，所以对于宽和高都应该是充满整个屏幕的，指定为fill_parent。

>注意：从Android2.2开始，为了更好的使用，fill_parent被改为match_parent。因为当我们把一个子部件设置为fill_parent之后，该部件不是占有同等级部件剩余的空间，而是和同等级部件重叠在一起。相反，使用match_parent则不会出现重叠的现象。

**添加一个文本输入框**

在线性布局了里，添加一个元素就可以创建一个用户可编辑的文本框，EditText类属于View的一个用于展示可编辑的文本的子类。

和View的别的类一样，你需要设置XML里的某些属性来指定EditText的具体功能，下边是你应该在线性布局里指定的一些属性元素：

	<EditText android:id="@+id/edit_message"
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:hint="@string/edit_message" />


关于一些属性的说明：

+	Android：id

	这里定义的是View的唯一标示符，你可以在程序的代码里进行引用，你可以对这个类进行读和修改的操作(在下一课里将会用到)
当你想从XML里使用资源类的时候必须使用@符号，紧随@之后的是资源的类型(这里是id)，然后是资源的名字(这里使用的是edit_message)。(其他的资源可以使用相同的名字只要他们不是相同的资源类型，例如：字符串资源可以使用相同的名字)。

	+号只是当你第一次定义一个资源ID的时候需要。这里是告诉SDK此资源ID需要被创建出来。在应用程序被编译之后，SDK就可以直接使用ID值，edit_message是在项目gen/R.java文件中创建一个新的标示符，这个标示符就和EditText关联起来了。一旦资源ID被创建了，其他资源如果引用这个ID就不再需要+号了，。这里是唯一一个需要+号的属性。可以参考右栏获取更多关于资源类的信息。

+	Android:layout_width 和android:layout_height

	对于宽和高不建议指定具体的大小，使用"wrap_content"指定之后，这个视图只是占据内容大小的空间。如果你使用了"fill_parent"，这时EditText将会布满整个屏幕，因为它将适应父布局的大小。想要看到更多信息，请参考XML 布局向导。

+	Android:hint

	当文本框为空的时候,会默认显示这个字符串。对于字符串"@string/edit_message"的值所引用的资源应该是定义在单独的文件里，而不是直接使用字符串。因为使用的是值是存在的资源，所以不需要使用+号。然而，由于你还没有定义字符串的值，所以在添加"@string/edit_message"时候会出现编译错误。下边你可以定义字符串资源值来去除这个错误。

**增加字符串资源**

当你在用户界面定义一个文本的时候，你应该把每一个文本字符串列入资源文件。对于所有字符串值，字符串资源能够单独的修改，在资源文件里你可以很容易的找到并且做出相应的修改。通过选择定义每个字符串，还允许您对不同语言本地化应用程序。

默认情况下，在res/values/string.xml里，你的Android项目包含一个字符串资源文件。打开这个文件，删除已经存在的"hello"字符串，为"edit_message"增加一个供使用的字符串值。

同时在这个文件里，再给button添加一个字符串，命名为"button_send".
下边就是定义好的string.xml文件内容：

	<?xml version="1.0" encoding="utf-8"?>
	<resources>
		<string name="app_name">My First App</string>
		<string name="edit_message">Enter a message</string>
    	<string name="button_send">Send</string>
	</resources>

**添加一个按钮**

紧跟后边，添加一个到布局里。

	<Button
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:text="@string/button_send" />

宽和高被设置为"wrap_content:，这时按钮占据的大小就是按钮里文本的大小。这个按钮不需要指定android:id的属性，因为在Activity代码里不被引用到。

**让输入框充满整个屏幕的宽度**

当前EditText和Button部件只是适应了他们各自内容的大小。

这样设置对按钮来说很合适，但是对于文本框来说就不太好了，因为用户肯能输入更长的文本内容，需要在左边留有一定的空白空间。因此如果能够沾满整个宽度会更好。LinearLayout使用权重的属性来达到这个目的，你可以使用android:layout_weitht属性来设置。

你可以根据每一个部件所占的空间来指定圈中值的大小，它的总数是有同级别的部件来决定的。就类似于饮料的成分配方：“两份伏特加酒，一份咖啡利口酒”，意思就是这个酒中伏特加酒占三分之二。例如，你设置一个View的权重是2，另一个View的权重是1，那么总数就是3，这时第一个View占据2/3的空间，第二个占据1/3的空间。如果你再加入第三个View，权重设为1，那么第一个View会占据1/2的空间，剩余的被另外两个View平分。

对于所有的View默认的权重是0，如果你只设置了一个View的权重大于0，那么这个View将占据除去别的View本身占据的空间的的所有剩余空间。因此这里设置EditText的权重为1，使其能够占据除了按钮之外的所有空间。

	<EditText
		android:layout_weight="1"
		... />

为了达到更有效的布局，在你设置权重的时候，你应该把EditText的宽度设置为0。如果你设置为"wrap_content"作为宽度，系统需要自己去计算这个部件所占有的宽度，而此时的因为你设置了权重，所以系统自动回占据剩余空间，EditText的宽度最终成了不起作用的属性。

	<EditText
		android:layout_weight="1"
		android:layout_width="0dp"
		... />

EditText设置了权重，因此占据了整个LinearLayout的剩余空间大小。

现在看一下完整的布局文件内容。

	<?xml version="1.0" encoding="utf-8"?>
	<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
		android:layout_width="fill_parent"
		android:layout_height="fill_parent"
		android:orientation="horizontal">
	<EditText android:id="@+id/edit_message"
		android:layout_weight="1"
		android:layout_width="0dp"
		android:layout_height="wrap_content"
		android:hint="@string/edit_message" />
    <Button
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:text="@string/button_send" />
	</LinearLayout>

整个布局默认被Activity类使用，Activity类是在你创建一个项目的时候SDK工具自动生成的，你可以直接运行app查看运行结果。

在Eclipse，点击工具栏里的Run。

#### 4. 启动另一个Activity

在完成上一课(构建简单用户接口)后，你已经拥有了显示一个activity（唯一屏幕）的app（应用），并且这个activity包含了一个文本字段和一个按钮。

在这节课中，你将会添加一些新的代码到MyFirstActivity中，当用户点击发送(Send )按钮时启动一个新的activity

**Respond to the Send Button-响应Send(发送)按钮**

响应按钮的on-click(点击)事件，打开main.xml布局文件然后在Button(按钮)元素中添加android:onclick属性:
 
	<Button 
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:text="@string/button_send"
		android:onClick="sendMessage" />
 
android:onclick属性的值：sendMessage就是当用户点击你屏幕按钮时触发方法的名字。

添加相应的方法在MyFirstActivity类中：
 
	/** 当用户点击Send按钮时调用 */
	public void sendMessage(View view) {
	// 做一些相应按钮的操作
	}
 
>注意：在Eclipse中，按Ctrl + Shift + O 可以导入缺失的类(在Mac中使用Cmd + Shift + O )

请注意，为了让系统能够将这个方法（你刚在MyFirstActivity中添加的sendMessage方法）与在android:onClick属性中提供的方法名字匹配，它们的名字必须一致，特别是，这个方法必须满足以下条件：

+	公共的
+	没有返回值
+	有一个唯一的视图（View）参数（这个视图就是将被点击的视图）

接下来，你可以在这个方法中编写读取文本内容的代码，并将该内容传到另一个Activity

**Build an Intent-构建一个Intent(意图)**

Intent(意图)是在不同组件中提供运行时连接的对象(比如两个Activity)。Intent(意图)代表一个应用"想去做什么事"，你可以用它做各种各样的任务，不过大部分的时候他们被用来启动另一个Activity。在sendMessage()方法中创建一个Intent(意图)并启动名为DisplayMessageActivity的Activity：
 
	Intent intent = new Intent(this, DisplayMessageActivity.class);
 
在这个Intent构造函数中有两个参数： 第一个参数是Context(上下文)(之所有可以用this是因为当前Activity(MyFirstActivity)是Context的子类) 系统需要传递Intent的应用组件的class对象（在这个案例中，这个activity应该被启动）

>注意：如果你正在使用的是类似Eclipse的IDE，这里对DisplayMessageActivity的引用会报错，因为这个类还不存在；注意这个错误，你很快就要去创建这个类了。

一个Intent(意图)不仅允许你启动另一个Activity，同时也可以传递一个数据包到另一个Activity，ok，用findViewById()方法得到EditText元素，然后将它的信息添加到Intent(意图):
 
	Intent intent = new Intent(this, DisplayMessageActivity.class);
	EditText editText = (EditText) findViewById(R.id.edit_message);
	String message = editText.getText().toString();
	intent.putExtra(EXTRA_MESSAGE, message);

**Sending an intent to other apps-发送intent(意图)到其他app(应用)**

>在这课中创建的Intent(意图)包含了一个非常明确的意图，因为它指定了一个Intent需要的精确app(应用)组件； 然而，在Intent没有指定明确的组件时，Intent(意图)是隐式的，但它允许安装在设备上的任何应用来回应， 只要这个应用满足在各个Intent(意图)参数中指定的action（行动）的元数据规范，想了解更多信息， 可以去看Interacting with Other Apps课程

Intent(意图)可以传递各种各样的以键值对形式出现的集合，可以称它为extras，putExtra()方法用字符窜作为它的key，第二个参数作为它的值为了在下一个Activity中获取extra(附加的)数据，你应该定义一个公共常量作为key(键),ok，在MyFirstActivity类的顶部定义一个名为EXTRA_MESSAGE的常量：

	public class MyFirstActivity extends Activity {
	public final static String EXTRA_MESSAGE = "com.example.myapp.MESSAGE";
	...
	}
 
为使extras键唯一，使用你应用的包名作为extras键的前缀是一个很好的做法，因为你的应用可能需要跟其他应用交互。

**Start the Second Activity-启动第二个Activity**

启动一个Activity，你只需要调用startActivity()方法然后传入你的Intent(意图)系统接收到你的请求后会实例化在Intent中指定的Activity,包含这个方法拥有的，被Send(发送)按钮调用的完整sendMessage()方法现在就像这样：
 
	/** 当用户点击Send按钮时调用 */
	public void sendMessage(View view) {
	Intent intent = new Intent(this, DisplayMessageActivity.class);
	EditText editText = (EditText) findViewById(R.id.edit_message);
	String message = editText.getText().toString();
	intent.putExtra(EXTRA_MESSAGE, message);
	startActivity(intent);
	}
 
现在你需要去创建一个DisplayMessageActivity支持程序能够执行起来

**Create the Second Activity-创建第二个Activity**

在你的项目中，在src/<package-name>/路径下新建一个名为DisplayMessageActivity.java的类。

>注：在Eclipse中，在src/路径下点鼠标右键选中New > Class，输入DisplayMessageActivity，并且指定继承android.app.Activity 。
在这个类中，添加onCreate()回调方法：

	public class DisplayMessageActivity extends Activity {
	@Override
		public void onCreate(Bundle savedInstanceState) {
			super.onCreate(savedInstanceState);
		}
	}
 
所有Activity的子类都必须实现onCreate()方法，当系统创建Activity实例时就会调用该方法，这个方法是你必须定义activity布局以及初始化必要activity组件的地方。

**Add it to the manifest-将Activity加入manifest(清单)文件**

你必须在manifest(清单)文件，AndroidManifest.xml中使用<activity>元素声明你所有的Activity；因为DisplayMessageActivity是由一个明确的Intent(意图)调用的，所以它不需要任何intent filters(意图过滤器)(intent filters，你可以在manifest文件中声明MyFirstActivity的地方看到)如此DisplayMessageActivity就可以在<application>元素中用一句很简单的代码声明；
 
	<application ... >
		<activity android:name="com.example.myapp.DisplayMessageActivity" />
	...
	</application>
 
这个app(应用)现在就可以运行了，因为第一个Activity中的Intent现在可以解析DisplayMessageActivity类了，如果你现在运行app，点击Send(发送)按钮启动,第二个Activity，它不会显示任何东西；

**Receive the Intent-获取Intent(意图)**

每一个被Intent调用的Activity，不管用户将它导航到哪，你都可以在启动的Activity中通过getIntent()方法得到Intent以及Intent包含的数据。在DisplayMessageActivity类的onCreate()方法中，得到intent以及MyFirstActivity提供的附加信息：
 
	Intent intent = getIntent();
	String message = intent.getStringExtra(MyFirstActivity.EXTRA_MESSAGE);
 
**Display the Message-显示信息**

在屏幕上显示信息，创建一个TextView部件，并且使用setText()设置它的值，然后通过setContentView()方法将TextView作为root(根)视图添加到Activity的布局。

DisplayMessageActivity完整的onCreate()方法现在看起来如下：
 
	@Override
	public void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		// 从intent中获取信息
		Intent intent = getIntent();
		String message = intent.getStringExtra(MyFirstActivity.EXTRA_MESSAGE);
		
		// 创建TextView对象
		TextView textView = new TextView(this);
		textView.setTextSize(40);
		textView.setText(message);
	
		setContentView(textView);
	}
 
现在你可以运行app，在文本中输入信息，点击Send(发送)按钮，ok，现在就可以在第二Activity上看到信息了。