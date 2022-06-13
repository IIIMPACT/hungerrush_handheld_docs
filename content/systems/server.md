---
title: "Test Server Setup"
date: 2022-06-08T16:05:59+01:00
draft: false
weight: 2
description: Setup guides for the local test environment
---

## HungerRush Server (SandBox environment)

### Prerequisites
- On a windows server machine, make sure you have these installed.
  - [Microsoft SQL Server 2019 or higher](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
  - [Microsoft SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16)
  - [Visual Studio](https://visualstudio.microsoft.com/)
  - [.NET Framework 4.5](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net46)
  - [Database files](https://drive.google.com/drive/folders/1u19rCeIli36HxihrtaVSpT0I7Ue8XP6M?usp=sharing)
    - iiimpact users can access this link
  - Powershell or Windows Terminal.
- On a Mac computer, make use of Parallels virtual machine and install the above.


#### Key Repos

Make request to HungerRush to provide access to these repos on Azure Devops.

```shell
# hungerrush legacy app
https://dev.azure.com/HungerRush/ReventionMain/_git/POS/
```
```shell
# hunggerrush backend
https://dev.azure.com/HungerRush/ReventionMain/_git/RevServices
```

### Installation (backend)
- Unpack the `Install.zip` into `C:\Install`
- Start the power shell as the administrator
- Run `c:\install\install.bat`
- If there are no errors during this, import the database from the zip file into your MS SQL Management Studio.
- If there are errors, restart the process
- After importing, switch to `119` database in MS SQL Management Studio
- Add a new SQL user with rights to this database 119:
    - username: `Revention`
    - password: `Astr0s`
    
- If user already exists within database, remove first and add user
- Enable `SQL authorization`
- Check that `RevControlSvc` is running
    - If not, open the file `C:\Revention\ReventionPOS.exe.config`
    - Set `SQLServer` to `SQL authorization`, 
    - Set `DBName` to `119`
    - Reboot service or server
- In the `119` databse, open `BusinessTable` table.
    - Set `AboveStoreID` to `999998` 


### Installation (legacy app)
- Open first instance of Visual Studio
- Open `RevServices\Main\Source\RevServicesCloudAPISln`
- Set `TestHost` as a startup project
- Run/Debug `TestHost`

- Open second instance of Visual Studio
- Open `POS\Main\Source\RevCloudPOS` solution
- Launch the `RevCloudPOS UWP project`
- Connect to `127.0.0.1` with password `999998` 


#### Credentials
These credentials can be used to progress through the manager signup and waiter login screens.

```shell
# ReventionId or Manager password
999998
```
```shell
# waiter login
1
```
