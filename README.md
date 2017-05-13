### Create Oracle users/schemas as follows:

appuser
* CREATE USER appuser IDENTIFIED BY appuser DEFAULT TABLESPACE datasmall TEMPORARY TABLESPACE temp;\
* GRANT connect,resource,create view TO appuser;

appdeploy
* CREATE USER appdeploy IDENTIFIED BY appdeploy DEFAULT TABLESPACE datasmall TEMPORARY TABLESPACE temp;
* GRANT all privileges TO appdeploy;
* GRANT select on dba_objects to appdeploy;
* GRANT select on dba_tab_privs to appdeploy;
