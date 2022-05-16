# Bases-Fonte - Criando o espaço e o usuário Schema
Script SQL para criar as bases fonte

Create tablespace TBS_SOURCE
logging datafile '/u01/app/oracle/oradata/orcl/TBS_SOURCE.dbf'
size 1m autoextend on next 10m maxsize unlimited extent management local segment auto;

#Criando o usuário para ser o Schema(proprietário) das bases de dados fonte:

create user source identified by source0123;
grant connect, resource to source;
grant unlimited tablespace to source;
