# Servlet-没必要细学，但有助于框架底层的理解
不错的一篇入门介绍(https://www.cnblogs.com/tanghaorong/p/12713000.html)  
是一个实现了servlet接口并重写doGet\doPost方法的特殊类。spring、springMVC等框架底层也是servlet  
一个应用有多个servlet，一个servlet对于一个服务  
位于服务端，客户端与数据库的中间。接收http请求，并相应处理(包括操作数据库)，封装http响应并返回给客户端  
从理解上-我感觉就是一个最低配的service层实现  ？   

# java四大域对象
1. page(jsp有效)------》page域指的是pageContext  
2. request(一次请求)---》request域request HttpServletContext  
3. session(一次会话)---》session域session HttpSession  
4. application(当前web应用)---》application域指的是application  ServletContext  