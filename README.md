# ⚡ ASP.NET MASTER GUIDE  
## 🚀 Beginner → Advanced → Pro Web Development (C# .NET)

---

# 📖 What is ASP.NET?

### English
ASP.NET is a powerful web framework developed by Microsoft for building dynamic websites, APIs, and enterprise applications using C#.

### বাংলা
ASP.NET হলো Microsoft-এর তৈরি একটি শক্তিশালী web framework, যা দিয়ে website, API, ERP এবং enterprise system তৈরি করা যায় C# ব্যবহার করে।

---

# 🌟 Why ASP.NET?

- ⚡ High Performance
- 🔐 Built-in Security
- 🏗️ MVC Architecture
- 🌐 REST API Support
- 🚀 Enterprise Level Applications
- 📦 Scalable Backend System

---

# 🛠️ INSTALLATION

## Install .NET SDK

```bash
dotnet --version
```

👉 Download:
https://dotnet.microsoft.com/

---

# 🚀 CREATE PROJECT

## ASP.NET MVC

```bash
dotnet new mvc -n MyApp
```

---

## Web API

```bash
dotnet new webapi -n MyApi
```

---

## Run Project

```bash
cd MyApp
dotnet run
```

👉 Open:
```
http://localhost:5000
```

---

# 📁 PROJECT STRUCTURE

```
MyApp/
 ├── Controllers/
 ├── Models/
 ├── Views/
 ├── wwwroot/
 ├── Program.cs
 ├── appsettings.json
```

---

# ⚙️ BASIC CONTROLLER

```csharp
using Microsoft.AspNetCore.Mvc;

public class HomeController : Controller
{
    public IActionResult Index()
    {
        return View();
    }
}
```

---

# 🌐 ROUTING

```csharp
app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");
```

---

# 📦 MVC ARCHITECTURE

```
Model → View → Controller
```

---

# 🗄️ DATABASE (Entity Framework)

## Install EF Core

```bash
dotnet add package Microsoft.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
```

---

## DB Context

```csharp
using Microsoft.EntityFrameworkCore;

public class AppDbContext : DbContext
{
    public DbSet<User> Users { get; set; }
}
```

---

## Model

```csharp
public class User
{
    public int Id { get; set; }
    public string Name { get; set; }
}
```

---

## Migration

```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```

---

# 🌐 ASP.NET WEB API

## Controller

```csharp
[ApiController]
[Route("api/users")]
public class UserController : ControllerBase
{
    [HttpGet]
    public IActionResult GetUsers()
    {
        return Ok(new { message = "API Working" });
    }
}
```

---

# 🔐 AUTHENTICATION (JWT)

## Install

```bash
dotnet add package Microsoft.AspNetCore.Authentication.JwtBearer
```

---

## Generate Token (Basic Idea)

```csharp
var token = "your-jwt-token";
```

---

# 🔁 CRUD OPERATIONS

## CREATE

```csharp
_context.Users.Add(user);
_context.SaveChanges();
```

---

## READ

```csharp
var users = _context.Users.ToList();
```

---

## UPDATE

```csharp
_context.Users.Update(user);
_context.SaveChanges();
```

---

## DELETE

```csharp
_context.Users.Remove(user);
_context.SaveChanges();
```

---

# 🌐 API TESTING FLOW

```
Frontend (React / Angular)
        ↓
ASP.NET API
        ↓
Entity Framework
        ↓
SQL Server Database
```

---

# ⚙️ COMMANDS

## Run Project

```bash
dotnet run
```

---

## Build Project

```bash
dotnet build
```

---

## Create Project

```bash
dotnet new mvc
dotnet new webapi
```

---

## EF Commands

```bash
dotnet ef migrations add Init
dotnet ef database update
```

---

# 🗄

---

## Installation

### Prerequisites
- [Git](https://git-scm.com/)
- The appropriate runtime/toolchain for this project

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/codexvisual/ASP.git
   cd ASP
   ```
2. Follow the project-specific setup (dependencies, environment variables, database, etc.).
3. Build and run the project using its standard commands.
