
# https://liquibase.jira.com/browse/CORE-3428

# Example that includeAll does not work with subfolders in Liquibase 3.6.3

`mvn spring-boot:run`
`mvn test`

Table `person` not created (liquibase 3.6.3)
Ignored file: src/main/resources/db/nested/create-table.xml

`mvn spring-boot:run -Dliquibase.version=3.6.2`
`mvn test -Dliquibase.version=3.6.2`

> 2019-06-02 18:36:34.470  INFO 8215 --- [           main] liquibase.executor.jvm.JdbcExecutor      : CREATE TABLE PUBLIC.person (address VARCHAR(255))