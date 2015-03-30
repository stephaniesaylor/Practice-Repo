##Add users and stewards to a test implementation
In an implementation, the system’s security determines users’ roles. In a development environment, you may want to create various users and roles in order to test the software. Never use these instructions to create users in a production environment because the passwords are not stored safely or encrypted. That said, use the following instructions to create test users in a development system:


1. From your Apache-tomcat directory, open the lib directory. 
2. In the `lib` directory, open the `users.properties` file.
3. Add users and roles based on the examples following these instructions.
4. Save changes to the `users.properties` file.
5. Restart `startup.bat` or `startup.sh` in the `Apache-tomcat-7.0.55\bin` directory. Each new user will appear in the system after you log in with it.

**User and Role Examples**
`testUser1=password,ROLE_USER,Test User 1,Test 1 Organization,testUser1@nowhere.com,[group1;I am a sample Group 1 from users.properties;test@gmail.com;active]`

`testSteward1=password,ROLE_USER:ROLE_ORG_STEWARD,Test Steward 1,Test 1 Organization,testSteward1@nowhere.com`

`testAdmin1=password,ROLE_ADMIN:ROLE_USER,Test Admin 1,Test Admin Organization,testAdmin1@nowhere.com,[group1;I am a sample Group 1 from users.properties;test@email.com;active]`
*Note: See the Steward section of the User and Steward Guide for further explanation of roles. *