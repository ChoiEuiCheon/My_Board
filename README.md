# My_Board
My Board Project<br>
Using Eclipse IDE<br>
launch with tomcat9.0<br>
recommended web.xml include this code : <br>

    <welcome-file-list>
    	<welcome-file>/WEB-INF/Login.jsp</welcome-file>
    	<welcome-file>/WEB-INF/Login.do</welcome-file>
    </welcome-file-list>
    
    <!-- FrontController URL Mapping -->
    <servlet>
    	<servlet-name>FC</servlet-name>
    	<servlet-class>com.korea.controller.FrontController</servlet-class>
    </servlet>
    <servlet-mapping>
    	<servlet-name>FC</servlet-name>
    	<url-pattern>*.do</url-pattern>
    </servlet-mapping>
    
    <!-- Filter URL Mapping   -->
    <filter>
		<filter-name>authority</filter-name>
		<filter-class>com.korea.filter.authfilter</filter-class>    
    </filter>
    <filter-mapping>
 		<filter-name>authority</filter-name>   
    	<url-pattern>*.do</url-pattern>
    </filter-mapping>
