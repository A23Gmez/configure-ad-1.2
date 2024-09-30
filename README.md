# # Configuring-AD Part 1.2

<h1>Deploying Active Directory</h1>

![image](https://github.com/user-attachments/assets/3b32e7e9-8b18-4233-8a94-dde8afc44543)

<h2>Install Active Directory: Part 1</h2>
<h3>Install Active Directory</h3>

![image](https://github.com/user-attachments/assets/c987f1a4-c0ac-4d9c-a97a-6964b23f4ebe)

- Login to DC-1 and install Active Directory Domain Services

  ![image](https://github.com/user-attachments/assets/4e5930ba-2d69-481e-8db0-7ff88effc5e7)

- DC: Setup a new forest as mydomain.com
- Restart and then logged back into DC-1 as user: mydomain.com\labuser

<h3>Create a Domain Admin user within the domain</h3>

![image](https://github.com/user-attachments/assets/32fdf946-f960-4f19-967d-15b2e2f62cbe)

- In Active Directory Users and Computers (ADUC), created an Organizational Unit (OU) called “_EMPLOYEES”
- Create a new OU named “_ADMINS”

![image](https://github.com/user-attachments/assets/0d8d5d9b-8332-4dbf-9d70-7058d59f604b)

![image](https://github.com/user-attachments/assets/34eb37ac-e137-41fa-8339-eb7a1ecda7b2)

![image](https://github.com/user-attachments/assets/5fa93f88-ab98-4723-8526-9fd680b6e605)

- Create a new employee named “Jane Doe” with the username of “jane_admin”
- Add jane_admin to the “Domain Admins” Security Group

![image](https://github.com/user-attachments/assets/c4240619-3917-4344-a0eb-e7476716b95f)

  - Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”


<h3>Join Client-1 to your domain (mydomain.com)</h3>

![image](https://github.com/user-attachments/assets/42e75c6f-fe42-44d2-8cca-bf50e85330e4)


- Set Client-1’s DNS settings to the DC’s Private IP address (Already done in a previous lab)
- Login to Client-1 as the original local admin (labuser) and join it to the domain (computer will restart)

![image](https://github.com/user-attachments/assets/940fb5c0-0a76-42e4-b29c-dfc9252a25f4)

- Login to the Domain Controller and verify Client-1 shows up in ADUC

![image](https://github.com/user-attachments/assets/51db90ba-c92c-4552-a32c-b6614b9c3e70)

-Create a new OU named “_CLIENTS” and drag Client-1 into the new OU _CLIENTS





