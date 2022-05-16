# Bases-Fonte - Criando o espaço e o usuário Schema
Script SQL para criar as bases fonte

CREATE TABLESPACE TBS_SOURCE
LOGGING DATAFILE '/u01/app/oracle/oradata/orcl/TBS_SOURCE.dbf' 
SIZE 1M AUTOEXTEND ON NEXT 10M MAXSIZE UNLIMITED EXTENT MANAGEMENT LOCAL SEGMENT SPACE MANAGEMENT AUTO;   


#Criando o usuário para ser o Schema(proprietário) das bases de dados fonte:

CREATE USER source IDENTIFIED BY source0123;
GRANT CONNECT, RESOURCE TO source;
GRANT UNLIMITED TABLESPACE TO source;  
