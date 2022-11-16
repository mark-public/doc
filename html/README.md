## input元素所有type类型及相关作用(共23种)

随着HTML5的出现，input表单元素新增了多种输入控件，用以接受各种类型 的用户输入。其中text、password、radio、checkbox、button、submit、reset、image、hidden、file这10个是传统的输入控件，HTML新增的输入控件包括url、tel、search、email、color、number、range、month、week、date、time、datetime、datetime-local共13个。  

常用的并且能为大多数浏览器所识别的类型大概有：text、password、number、button、reset、submit、hidden、radio、checkbox、file、image、color、range、date、month、week、time、datetime-local。  

另外还有一些类型：tel、email、url、datetime、search。这些类型部分浏览器不支持识别或校验。  


### 传统控件
1、type='text': 创建单行文本输入框（默认的输入类型） 
   文本输入框，是一个单行的控件，一般是带有内嵌框的矩形
```html
<input type="text" size="30" maxlength="20" placeholder="请输入搜索关键字" />
```
上面代码意思是：input元素类型为文本输入框;元素长度等于30;最多只能输入20字符;输入框中提示用户内容为“请输入搜索关键字”  

<br />


2、type='password': 密码输入框
 密码输入框，与文本输入框基本一模一样，功能上唯一的不同是字母输入后会被隐藏，一般是用小黑点代替  
```html
<input type="password" size="10" maxlength="10"  />
```
上面代码意思是：input元素类型为密码输入框;元素长度等于10;最多只能输入10字符  
<br />
  
3、type='radio': 单选按钮
  单选按钮，允许用户从给定数目的选择中选一个选项，同一组选项按钮，name值一定要一致
```html
男<input type="radio" value="男" name="single" />
女<input type="radio" value="女" name="single" checked />
人妖<input type="radio" value="人妖" name="single"  />
```
上面代码意思是：input元素类型为单选按钮;其中value属性中的值用来设置用户选中该项目后提交到数据库中的值；拥有相同name属性的单选框为同一组，一个组里只能同时选中一个选项；而checked属性表示的是初始选项，在用户还没进行选中之前，初始值会选中“女”这个项目

<br />
4、type='checkbox': 复选框
复选框，允许用户从给定数目的选择中选一个或多个选项，同一组选项按钮，name值一定要一致
```html
广州<input type="checkbox" value="广州" name="city" />
深圳<input type="checkbox" value="深圳" name="city" />
杭州<input type="checkbox" value="杭州" name="city" />
北京<input type="checkbox" value="北京" name="city" />
```
上面代码意思是：input元素类型为复选框;用户可以进行多个选项，其中value属性中的值用来设置用户选中该项目后提交到数据库中的值；name为控件的名称

<br />
5、type='button': 普通按钮
  普通按钮，定义可点击的按钮，但没有任何行为，常用于用户点击时调用JavaScript方法
```html 
<input type="button" value="喜欢请点个赞吧" name="btn" onClick=""  />
```
上面代码意思是：input元素类型为普通按钮;在value属性中输入的值为按钮上显示的文本；name代表该按钮的名称；onclick表示处理程序

<br />
6、type='submit': 提交按钮
  提交按钮，用于创建提交表单的按钮
```html
<input type="submit" value="提交" name="subBtn"  />
```
上面代码意思是：input元素类型为提交按钮;提交按钮不需要设置onclick参数，在单击提交按钮时可以向服务器发送表单数据，数据会发送到表单的 action 属性中指定的页面；value属性中的值为按钮上显示的文字

<br />
7、type='reset': 重置按钮
  重置按钮，用于创建重置表单的按钮
```html
<input type="reset" value="重置按钮" name="reset"  />
```
上面代码意思是：input元素类型为重置按钮;重置按钮的作用是点击之后表单会刷新回到默认状态，在value属性中输入的值为按钮上显示的文本

<br />
8、type='image': 图像按钮   
 图像按钮，该类型可以设置width、height、src、alt这四个属性用图片作为提交按钮会一起发送点击在图片上的x和y坐标，这样可以与服务器端图片地图结合使用，如果图片有name属性，也会随坐标发送
```html
<input type="image" src="" name="确定" width="90" hieght="30" />
```
上面代码意思是：input元素类型为图像按钮;虽然显示是图片，实际是以图片的形式按钮；其中src是链接图片的路径；name为图片名称；width图片宽度；height图片高度；当按下图像按钮会以name中的值向服务器发送信息

<br />
9、type='hidden': 隐藏域
  隐藏域，定义隐藏输入类型用于在表单中增加对用户不可见，但需要提交的额外数据时，disabled属性无法与type="hidden"的input元素一起使用
```html
<input type="hidden" name="hidden" value="提交的值"  />
```
上面代码意思是：input元素类型为隐藏域;隐藏域在页面上不显示，用来存储与传递表单的值，当用户提交表单时，隐藏域的内容会一起提交给处理程序

<br />
10、type='file': 文件域
  文件，用于文件上传，
```html
<input type="file" name="file"  accept="image/png,image/jpg,image/gif,image/JPEG" />
```
上面代码意思是：input元素类型为文件域; accept属性表示可上传提交的文件类型

<br />
<br />
### H5新增控件
```
1、type='url': 输入URL字段
  会自动验证url域的值，外观上与type="text"的input输入类型没有差异  [注意]IE9-浏览器及safari浏览器不支持
```html
<input type="url" />
```
<br />

2、type='tel': 用来输入电话号码
  用于表示语义上的电话输入域，外观上与type="text"的input输入类型没有差异，在手机端会唤出数字键盘
```html
<input type="tel" name="tel" />
```
<br />


3、type='search': 搜索字符串
  用于表示语义上的搜索框，外观上与type="text"的input输入类型没有差异，在手机端会唤出搜索按键
```html
<input type="search"  />
```
<br />

4、type='email': 输入“email”地址
  用于表示语义上的e-mail地址输入域，会自动验证email域的值，外观上与type="text"的input输入类型没有差异，在手机端会唤出英文键盘，email支持multiple属性  [注意]IE9-浏览器及safari浏览器不支持
```html
<input type="email" />
```
上面代码意思是：input元素类型为email地址;若用户输入的非email格式，那么在支持HTML5的浏览器中提交该表单时，会提示为不是合法格式
<br />

5、type='color': 颜色选择器
 颜色选择器，该类型会创建一个调色板用来选择颜色，颜色值以URL编码后的十六进制数值提交。如黑色会以%23000000发送，其中%23是#的URL编码。  [注意]safari和IE不支持该类型
```html
<input type="color" id="color" />
```
上面代码意思是：input元素类型为颜色控件;使用color属性能直接调用系统的颜色调节窗口，默认为黑色
<br />

6、type='number': 数字字段
 用于处理数字输入，在手机端会唤出数字键盘  [注意]IE不支持该类型
```html
<input type="number" name="number" min="2" max="10" value="3"  />
```
上面代码意思是：input元素类型为数字字段;用于输入数字的字段，其中min设定允许的最小值；max设定允许的最大值；value规定默认值；还有step可规定合法数字间隔
<br />

7、type='range': 输入数字控件   
用于处理包含在一定范围内的数字输入，类似于type="number"的input类型  [注意]IE9-不支持该类型
```html
<input type="range" name="range" min="0" max="10" step="1" value="" />
```
上面代码意思是：input元素类型为输入数字控件;min属性指定最小值限制，max属性指定最大值限制，step属性规定合法数字间隔，value属性规定默认值
<br />

8、type='month': 年月控件
 用于选取月、年
```html
<input type="month" value="2018-11" />
```
上面代码意思是：input元素类型为年月控件;value属性用来控制年月
<br />

9、type='date': 日期控件
 用于选取日、月、年
```html
<input type="date" min="2018-01-01" max="2020-01-01" />
```
上面代码意思是：input元素类型为日期控件;可用来选择或输入日期，包括（年/月/日）不包括时间；其中设定 min 属性控制开始日期，max 属性控制结束日期
<br />

10、type='datetime': 日期加时间控件（基于UTC时区）
  用于选取时、日、月、年(UTC时间)
```html  
<input type="datetime" value="2018-11-30T22:47Z" />
```
上面代码意思是：input元素类型为日期加时间控件;创建日期时间，包括（年/月/日/时/分/秒/零点几秒）
<br />

11、type='datetime-local': 日期加时间控件（不带时区）
 用于选取时、日、月、年(本地时间)
```html
<input type="datetime-local" value="2018-11-21 22:47"  />
```
上面代码意思是：input元素类型为日期时间控件;创建本地日期时间，包括（年/月/日/时/分/秒/零点几秒）
<br />

12、type='time': 时间控件
 用于选取时、分
```html
<input type="time" />
```
<br />

13、type='week': 周年控件
用于选取周、年
```html
<input type="week" />
```
