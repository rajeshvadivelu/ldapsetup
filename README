README:

--------


# sh configure_local_ldap.sh -h

usage: configure_local_ldap.sh [options]


This script assists in setting up local ldap for CTF.

OPTIONS:

-h,--help Show this message

-i,--install Installs and configurs openldap

-b,--bootstrap Sets new OU,DN and groups

-u,--adduser Adds user to the default group


For fresh setup:

---------------

1. This step will install openldap, openldap-servers, openldap-client from the yum repository.

And starts the slapd service.

sh configure_local_ldap.sh -i

2. This step will create default DC, OU, Users and Group

sh configure_local_ldap.sh -b

3. Repeat this user creationg step to create as many users as needed.

sh configure_local_ldap.sh -u

4. Run below command to review the entire LDAP content

ldapsearch -x -LLL -b dc=local,dc=dom -h localhost -p 389

5. Stop slapd service

service slapd stop

6. Move /var/lib/ldap to /opt/collabnet/teamforge/var

7. Symlink /opt/collabnet/teamforge/var/ldap to /var/lib/ldap

8. Start slapd service

This will ensure that the local ldap db is always in netapp and not lost during migrations.



9. Following configurtaion needs to be added to standalone-full.xml either manually or via the authentication manager.



<login-module code="org.jboss.security.auth.spi.LdapLoginModule" flag="sufficient">

<module-option name="java.naming.factory.initial" value="com.sun.jndi.ldap.LdapCtxFactory"/>

<module-option name="java.naming.security.authentication" value="simple"/>

<module-option name="allowEmptyPasswords" value="false"/>

<module-option name="java.naming.provider.url" value="ldap://localhost:389/"/>

<module-option name="principalDNSuffix" value=",ou=Users,dc=local,dc=dom"/>

<module-option name="principalDNPrefix" value="uid="/>

<module-option name="throwValidateError" value="true"/>

</login-module>



--------------------------------------------------



For upgrade / migration:

-----------------------

1. This step will install openldap, openldap-servers, openldap-client from the yum repository.

And starts the slapd service.



sh configure_local_ldap.sh -i



2. Move /var/lib/ldap as /var/lib/ldap.org



3. Symlink /opt/collabnet/teamforge/var/ldap to /var/lib/ldap



4. Start slapd service



service slapd start



5. Following configurtion needs to be added to standalone-full.xml either manually or via the authentication manager.



<login-module code="org.jboss.security.auth.spi.LdapLoginModule" flag="sufficient">

<module-option name="java.naming.factory.initial" value="com.sun.jndi.ldap.LdapCtxFactory"/>

<module-option name="java.naming.security.authentication" value="simple"/>

<module-option name="allowEmptyPasswords" value="false"/>

<module-option name="java.naming.provider.url" value="ldap://localhost:389/"/>

<module-option name="principalDNSuffix" value=",ou=Users,dc=local,dc=dom"/>

<module-option name="principalDNPrefix" value="uid="/>

<module-option name="throwValidateError" value="true"/>

</login-module>

