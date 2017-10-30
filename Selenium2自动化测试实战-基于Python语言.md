#定位元素#

1. ID定位
find_element_by_id("kw")

2. name定位
find_element_by_name("wd")

3. class定位
find_element_by_class_name("s_ipt")

4.tag定位
find_element_by_tag_name("input")

5. link定位
find_element_by_link_text("新闻")

6. partial link

这是对link定位的一种补充，有些文本链接会比较长，这时候可以去文本连接的一部分定位
find_element_by_partial_text("一个很长的")

7. XPath定位

XPath有多种定位策略

 7.1. 绝对路径定位
find_element_by_xpath("/html/boby/div/div[2]/div/div/div/from/span/input")

 7.2 利用元素属性定位
find_element_by_xpaht("//input[@id='kw']")
//表示当前页面某个目录下，
input表示定位元素的标签名
[@id='kw']表示这个元素的ID属性值等于kw

fing_element_by_xpath("//input[@name='wd']")
fing_element_by_xpath("//input[@class='s_ipt']")
find_element_by_xpath("//*[class='bg_s_btn']")
如果不想制定标签名，则可以用星号（*）代替

 7.3. 层级与属性结合
find_element_by_xpath("//span[@class='bg_s_ipt_wr']/input")
span[@class='bgs_ipt_wr']通过class属性定位到父元素，
后面/input表示父元素下面的子元素
如果父元素没有可利用的属性值，可继续向上查找“爷爷”属性
find_element_by_xpath("//form[@id='form']/span/input")
find_element_by_xpath("//form[@id='form']/span[2]/input")

8. 使用逻辑运算符
find_element_by_xpath("//input[@id='kw' and @class='su']/span/input]")

9.CSS(Cascading style sheets)定位

CSS是一种语言

|选择器|例子|描述|
|-|-|-|
|.class|.intro|class选择器，选择class=“intro”的所有元素|
||||




































