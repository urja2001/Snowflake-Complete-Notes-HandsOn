# Types of Roles & Securable Objects in Snowflake  ❄️

## 2 Types of Roles Snowflake 

### 1. System-Defined Roles     2. Custom Roles

### 1. System-Defined Roles

<b> ORGADMIN :</b> At the organisational level, this is a role that manages operation. i.e. Manages at organization-level operations and account visibility.

<b> ACCOUNTADMIN : </b> The ACCOUNTADMIN position combines the SYSADMIN and SECURITYADMIN responsibilities into one i.e. Holds top-level privileges.

<b> SECURITYADMIN : </b> This position is responsible for monitoring and managing users and roles i.e Manages grants and user roles.

<b> USERADMIN :</b> This position is in charge of creating roles and users i.e Focuses on user and role management.
In similar words USERADMIN is same as SECURITYADMIN, only thing is USERADMIN can only create roles and users.

<b> SYSADMIN :</b> In an account, this role has the ability to construct warehouses, databases, and other objects. SYSADMIN is supposed to roll up all custom roles. i.e. Manages databases, schemas, and warehouses.

<b> PUBLIC :</b> This is a role that is automatically assigned to all users and roles in your account i.e. Grants basic access to all users.

<div align="center">
<img align="center" alt="Snowflake" src="https://github.com/urja2001/Snowflake-Complete-Notes-HandsOn/blob/8410a1f983eef712c2ee6e9b24653760e25c5653/Chapter%2000%20-%20Architecture%20of%20%20Snowflake/pics/RBAC2.jpg" width="500" height="400" style="border-radius:50%">
</div>

# Securable Objects in Snowflake

Every securable object is nested within a logical container in a hierarchy of containers. 
The ORGANIZATION is at the topmost container.
Individual secure objects such as TABLE, VIEW, STAGE, UDF, FUNCTIONS, and other objects are stored within a SCHEMA object, which is contained in a DATABASE, and all of the DATABASE are contained within the ACCOUNT object.

<div align="center">
<img align="center" alt="Snowflake" src="" width="500" height="400" style="border-radius:50%">
</div>
