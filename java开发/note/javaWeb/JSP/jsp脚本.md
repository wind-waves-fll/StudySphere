JSP脚本分类：
1. <%    %>:内容会之间放到 _jspService()方法中
2. <%=   %>:内容会放到out.print(),作为out.print()的参数
3. <%!   %>:内容会放到 _jspService()方法之外，被类直接包含

JSP缺点：
1. 书写麻烦，特别是复杂的页面
2. 阅读麻烦
3. 复杂度高：允许依赖各种环境，JRE,JSP容器，JavaEE
4. 占内存和磁盘：jsp会自动生成.java和.class文件占磁盘，运行的是.class文件占内存
5. 调试困难：出错后，需要找到自动生成的.java文件进行调试
6. 不利于团队协作：前端人员不会java，后端人员不精HTML

EL表达式：
- Expression Language表达式语言，用于简化JSP页面内的Java代码
- 主要功能：获取数据
- 语法：${expression}
- javaweb中的四大域对象
    1. page         当前页面有效
    2. request      当前请求有效
    3. session      当前会话有效
    4. application  当前应用有效

el表达式获取数据，会依次从这4个域中寻找，直到找到为止

JSTL标签：
使用标签啊取代JSP页面上的Java代码
<c:if test="">
</c:if>

<c:forEach>
<c:forEach item="" var="">
<c:forEach begin="0" end="10" step="1" var="">
</c:forEach>

1. 导入坐标
2. 在JSP页面上引入JSTL标签库

<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
3. 使用