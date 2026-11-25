# C# JSON User Store

A C# console application that **reads, adds and saves users in JSON files** with Newtonsoft.Json, including **inheritance-based typed objects**.

![C#](https://img.shields.io/badge/C%23-.NET%20Framework%204.7.2-512BD4?logo=dotnet) ![Newtonsoft.Json](https://img.shields.io/badge/Newtonsoft.Json-serialization-blue)

## What it does

1. **Reads** `users.json` and lists every user (name, age, city). If the file is missing, it creates an empty one.
2. **Adds** a new user and **saves** the list back to `users.json`.
3. **Creates typed users** (`UserWithRole`, e.g. Admin and User) and serializes them to `typed_users.json`.
4. **Deserializes** the typed file and prints each user with their role.

## Model

```
User           Name, Age, City
 ├── Admin          Role = "Admin"
 ├── RegularUser    Role = "User"
 └── UserWithRole   Role (set per user)
```

## Run

Open `oop project 1.csproj` in **Visual Studio**, restore the NuGet packages (Newtonsoft.Json) and press **F5**.

Example output:

```
Users from users.json:
Name: ..., Age: ..., City: ...

Added new user to users.json

Users from typed_users.json:
Admin: AdminUser, Age 45, City Vilnius
User: RegularJoe, Age 25, City Kaunas
```
