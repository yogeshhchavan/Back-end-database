# Back-end Database Devlopment 
# Zumba Enrollment System (Servlets + JSP + JDBC + MySQL)

## Prerequisites
- JDK 11+
- Apache Maven 3.6+
- MySQL 8+
- Apache Tomcat 9+

## Setup
1. Create DB and tables:
   ```sql
   -- Update credentials if needed; then run:
   SOURCE db/schema.sql;
   ```

2. Update database credentials in `src/main/webapp/WEB-INF/web.xml`:
   ```xml
   <context-param>
     <param-name>DB_URL</param-name>
     <param-value>jdbc:mysql://localhost:3306/zumba_db?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=UTC</param-value>
   </context-param>
   <context-param>
     <param-name>DB_USER</param-name>
     <param-value>root</param-value>
   </context-param>
   <context-param>
     <param-name>DB_PASSWORD</param-name>
     <param-value>password</param-value>
   </context-param>
   ```

3. Build:
   ```bash
   mvn clean package
   ```

4. Deploy the generated WAR `target/ZumbaEnrollmentSystem.war` to Tomcat (drop into `webapps/`).

5. Open: `http://localhost:8080/ZumbaEnrollmentSystem/`

## Features
- CRUD for Students and Batches
- Assign Students to Batches
- JSP views with JSTL
- DAO pattern with JDBC
