# Role Based Access Control in Snowflake  ❄️

<div align="center">
<img align="left" alt="Snowflake" src="https://github.com/urja2001/Snowflake-Complete-Notes-HandsOn/blob/651f506e9ce6a3792d99d2c4db0256e6b5e2de8a/Chapter%2000%20-%20Architecture%20of%20%20Snowflake/pics/Key%20Concepts%20in%20RBAC.jpg" width="480" height="400" style="border-radius:50%">
<img align="right" alt="Snowflake" src="https://github.com/urja2001/Snowflake-Complete-Notes-HandsOn/blob/42a442126d799a0baeeb0d721b4274a77fa9e4ba/Chapter%2000%20-%20Architecture%20of%20%20Snowflake/pics/Privilages%20in%20RBAC.jpg" width="490" height="400">
</div>
 
**Role** 

 o	Roles are the entities to which privileges on securable objects can be granted and revoked.<br>
 o	Roles are assigned to users to allow them to perform actions required for business function.<br>
 o	A user can be assigned multiple roles. This  allows users to switch roles.<br>
 o	On Snowflake web UI the top right corner shows which Role is currently user is using.<br>

##
**2 Types of Roles Snowflake <br>**

 **1. System-Defined Roles**     **2. Custom Roles**
---

**1. System-Defined Roles**
---

<b> 1) ORGADMIN (Organization Administrator):</b> At the organisational level, this is a role that manages operation. i.e. Manages at organization-level operations and account visibility.

Note :<br>
       o Can view all accounts in the organization using SHOW ORGANIZTION ACCOUNTS <br>
       o Also all regions are enabled for organization accounts using SHOW REGIONS <br>
       o Can view usage information across the organization.<br>

<b> 2) ACCOUNTADMIN (Account Administrator) : </b> The ACCOUNTADMIN position combines the SYSADMIN and SECURITYADMIN responsibilities into one i.e. Holds top-level privileges.

<b> 3) SECURITYADMIN (Security Administrator)  </b> This position is responsible for monitoring and managing users and roles i.e Manages grants and user roles.

<b> 4) USERADMIN (User and Role Administrator) :</b> This position is in charge of creating roles and users i.e Focuses on user and role management.
In similar words USERADMIN is same as SECURITYADMIN, only thing is USERADMIN can only create roles and users.

<b> 5) SYSADMIN (System Administrator) :</b> In an account, this role has the ability to construct warehouses, databases, and other objects. SYSADMIN is supposed to roll up all custom roles. i.e. Manages databases, schemas, and warehouses.

<b> 6) PUBLIC :</b> This is a By Default Role that is automatically assigned to all users and roles in your account i.e. Grants basic access to all users.

<div align="center">
<img align="center" alt="Snowflake" src="https://github.com/urja2001/Snowflake-Complete-Notes-HandsOn/blob/8410a1f983eef712c2ee6e9b24653760e25c5653/Chapter%2000%20-%20Architecture%20of%20%20Snowflake/pics/RBAC2.jpg" width="500" height="500" style="border-radius:50%">
</div>

## 
**Securable Objects in Snowflake**

Every securable object is nested within a logical container in a hierarchy of containers. <br>
The ORGANIZATION is at the topmost container.<br>
Individual secure objects such as TABLE, VIEW, STAGE, UDF, FUNCTIONS, and other objects are stored within a SCHEMA object, which is contained in a DATABASE, and all of the DATABASE are contained within the ACCOUNT object.<br>


<div align="center">
<img align="center" alt="Snowflake" src="https://github.com/urja2001/Snowflake-Complete-Notes-HandsOn/blob/5968fd74abd7acf8503602f3dbccce0a5ffd719b/Chapter%2000%20-%20Architecture%20of%20%20Snowflake/pics/RBAC3.jpg" width="500" height="400" style="border-radius:50%">
</div>
