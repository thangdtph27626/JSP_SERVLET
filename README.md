<p align="center">
 <h2 align="center">Tạo web application JSP Servlet sử dụng JSTL với Tomcat10 </h2>
</p>

# Tạo project Java web application

new project -> jakarta EE -> Template -> web application -> create

![image](https://user-images.githubusercontent.com/109157942/209603258-7bcf6804-5935-448e-8c4c-242d6978024a.png)

![image](https://user-images.githubusercontent.com/109157942/209603282-9bea91ad-a936-42b5-ba27-218af85832d1.png)


# Thêm tomcat 

1: dowload tomcat 10 [tại đây](https://tomcat.apache.org/download-10.cgi)

Core -> click dowload 32 hoặc 64 bit -> giải nén file 

![image](https://user-images.githubusercontent.com/109157942/209603664-9eddcc68-db46-4eef-8e41-10a04ab312a0.png)

2: thêm tomcat 10 vào Intellij

![image](https://user-images.githubusercontent.com/109157942/209603534-e234f9ff-b288-4911-9825-e1bf386b34d9.png)


chọn edit configuration -> add new run configuration (hoặc dấu cộng trên cùng bên trái) -> tomcat server -> local 

![image](https://user-images.githubusercontent.com/109157942/209604015-300b7f00-c9d9-4ed0-ac69-0d20a2f7e2ee.png)
![image](https://user-images.githubusercontent.com/109157942/209604081-e39e7f20-326c-4e29-8754-fed90acd74ff.png)

![image](https://user-images.githubusercontent.com/109157942/209604207-26e566ed-a4fe-4422-9502-41fd1b96c4cc.png)

click chuột  configuration-> click dấu cộng -> click tomcat home -> trỏ tới folder vừa tải tomcat 10 -> ok ->  ok 

![image](https://user-images.githubusercontent.com/109157942/209604367-1ea45bf5-4fc9-468b-b97d-7d6d8840216c.png)


![image](https://user-images.githubusercontent.com/109157942/209604165-32aad9ba-e241-4885-9e37-15dea3b86eae.png)

Tại Before launch -> click dấu cộng -> Buid Arifacts -> chọn    tên folder:war exploded -> ok 

![image](https://user-images.githubusercontent.com/109157942/209604988-ef845f01-2732-4c4d-a4fe-815f0b16f42d.png)

Deployment -> dấu cộng -> Arifacts -> chọn    tên folder:war exploded 

![image](https://user-images.githubusercontent.com/109157942/209605228-037f84b5-9fb7-4765-8c58-6fdec52d2230.png)

Click OK 

> Thực hiện chạy file index.jsp

![image](https://user-images.githubusercontent.com/109157942/209605302-ecb3187f-120b-4052-b8c7-304ed187c281.png)


![image](https://user-images.githubusercontent.com/109157942/209605325-72ada8df-357c-49d0-a36f-be831eaceabb.png)


# configura trong pom xml thêm dependency 

```
<!-- taglibs-standard-spec-*.jar -->
        <!-- http://mvnrepository.com/artifact/org.apache.taglibs/taglibs-standard-spec -->
        <dependency>
            <groupId>org.apache.taglibs</groupId>
            <artifactId>taglibs-standard-spec</artifactId>
            <version>1.2.5</version>
        </dependency>
        <dependency>
            <groupId>javax.servlet.jsp.jstl</groupId>
            <artifactId>jstl-api</artifactId>
            <version>1.2</version>
        </dependency>
        <!-- taglibs-standard-impl-*.jar -->
        <!-- http://mvnrepository.com/artifact/org.apache.taglibs/taglibs-standard-impl -->
        <dependency>
            <groupId>org.apache.taglibs</groupId>
            <artifactId>taglibs-standard-impl</artifactId>
            <version>1.2.5</version>
        </dependency>

```


# Đăng ký thư viện JSP

khai báo taglib tại đầu trang jsp

```

<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>

```

# Kiểm Thử 

```
<body>
<c:set var = "stuff" value ="<%= new java.util.Date() %>" />
Time is ${stuff}
<h1><%= "Hello World!" %>
</h1>
<br/>
<a href="hello-servlet">Hello Servlet</a>
</body>

```


> tham khảo thêm các Tag [tại đây](https://www.tutorialspoint.com/jsp/jsp_standard_tag_library.htm)

# kêt quả 

![image](https://user-images.githubusercontent.com/109157942/209607173-063e0665-7062-4c0e-8cdb-799f7e2b378f.png)


> Toàn bộ code bài viết xem [tại đây](https://github.com/thangdtph27626/JSP_SERVLET.github.io)
