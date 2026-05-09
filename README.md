# Apartment Management System

## 📌 Overview

Apartment Management System is an ASP.NET Core MVC application developed to manage apartment blocks, flats, billing operations, user management, and internal messaging in a centralized system.

The project was built using a layered architecture approach with ASP.NET Identity authentication, Entity Framework Core, Repository Pattern, and Unit of Work Pattern.

---

## 🏗 Architecture

The solution follows a layered architecture:

- **UI Layer**
  - ASP.NET Core MVC (Razor Views)
  - Authentication & authorization
  - AJAX-based frontend interactions

- **Business Layer**
  - Business rules and service implementations
  - DTO-based communication

- **Domain Layer**
  - Core entities and enums
  - Base entity structures

- **EntityFramework Layer**
  - Entity Framework Core DbContext
  - Fluent API configurations
  - Repository & Unit of Work implementations

---

## 🔐 Authentication & Authorization

- ASP.NET Identity authentication
- Cookie-based authentication
- Role-based authorization (Manager / User)
- Protected endpoints using `[Authorize]`
- Seeded default users and roles

---

## 🎯 Features

### User & Role Management
- User CRUD operations
- Role assignment system
- Password reset functionality
- Role-based access control

### Apartment & Flat Management
- Apartment block management
- Flat management
- Flat type definitions

### Billing System
- Bill creation and distribution
- Monthly / yearly billing support
- Bill payment tracking
- Debt & payment reporting

### Messaging System
- Near real-time messaging using AJAX polling
- Notification support
- Unread message tracking

### Frontend Features
- AJAX-based CRUD operations
- Dynamic table operations
- Pagination & search (DataTables)
- Responsive admin panel UI

---

## ⚙️ Tech Stack

- ASP.NET Core MVC (.NET 5)
- ASP.NET Identity
- Entity Framework Core 5
- MSSQL Server
- Repository Pattern
- Unit of Work Pattern
- LINQ
- jQuery
- AJAX
- Bootstrap
- DataTables

---

## 🗄 Database

- MSSQL Server
- Code-First approach
- Fluent API entity configurations
- ASP.NET Identity integration

### Seeded Roles
- Manager
- User

### Seeded Users

| Email | Password | Role |
|---|---|---|
| manager@manager.com | `Sifre%5` | Manager |
| user@user.com | `Sifre%5` | User |

---

## 🚧 Missing / Incomplete Features

- Payment processing module in the API layer is still under development.
  

## 🚀 Getting Started

### Requirements

- .NET 5 SDK
- MSSQL Server
- Visual Studio

### Run

1. Clone the repository

```bash
git clone https://github.com/your-repo/apartment-management-system.git
```

2. Configure the connection string in `appsettings.json`

3. Apply migrations

```powershell
Update-Database
```

4. Run the project using Visual Studio

---

## 📷 Screenshots



> Note: The application interface is currently available in Turkish only.


# Login

- Login is performed using registered Email and Password. Validation checks are used for verification purposes.

<img width="840" alt="01 Login" src="https://user-images.githubusercontent.com/71590181/164468270-3f8445d3-27d2-4d48-ab74-aa735209f2e8.PNG">

<img width="897" alt="01 login 2" src="https://user-images.githubusercontent.com/71590181/164468654-596b14a6-930c-42bb-bb34-bad8dbf1e984.PNG">

# Home Page

- The project includes a collapsible left-side menu.

 <img width="903" alt="02 Ana Sayfa" src="https://user-images.githubusercontent.com/71590181/164469150-99e4899d-fb18-42d9-8225-d344ce1922d5.PNG">
 
 <img width="806" alt="02 Ana Sayfa 2" src="https://user-images.githubusercontent.com/71590181/164469190-a34f5eba-7a1f-4b62-b91a-fc5363c8cd9b.PNG">

# User Operations

- User add, update, and delete operations are performed by users with Manager role in the “Kimlik - Rol” page.
- Datatable is used for listing, enabling pagination and search functionality.
- Add, update, and delete operations are performed via AJAX without page refresh.
 
<img width="946" alt="03" src="https://user-images.githubusercontent.com/71590181/164470499-62bb6bd3-f0f9-41f0-8b0c-0973369a7085.PNG">

<img width="955" alt="03 1" src="https://user-images.githubusercontent.com/71590181/164470524-20753e5d-121d-46d4-be0e-0f00d1272b35.PNG">

- Vehicle management allows users to register multiple vehicles.
- Operations are handled via AJAX with search and pagination support.
<img width="956" alt="03 3" src="https://user-images.githubusercontent.com/71590181/164471313-b6b653a1-e07b-408d-9073-01c21108c679.PNG">




# Apartment / Flat Operations

- Apartment block management is handled in the “Blok” page.
- Supports listing, search, pagination, add, update, and delete operations.

<img width="956" alt="04 2" src="https://user-images.githubusercontent.com/71590181/164472412-493cdaf3-f061-40ff-a408-a3f71dcba4b1.PNG">

- Flat management is handled in the “Daire” page with similar functionality.
- All operations are performed using jQuery and AJAX without page refresh.

<img width="951" alt="05 " src="https://user-images.githubusercontent.com/71590181/164473090-7319e653-f774-4fbe-8d9e-3c26eb1d1e86.PNG">

<img width="934" alt="05 2" src="https://user-images.githubusercontent.com/71590181/164473468-582c9abe-d537-4e97-8200-85d0f68f7750.PNG">




# Invoice Operations

- Invoice creation, update, deletion, and distribution to flats are handled in the “Fatura Ekle-Dağıt” page.
- Invoices are created by year, month, and type, then distributed to flats.
 
<img width="960" alt="06 1" src="https://user-images.githubusercontent.com/71590181/164474949-693fec4a-f347-43e2-96c4-4049303e54e2.PNG">

<img width="948" alt="06 2" src="https://user-images.githubusercontent.com/71590181/164474970-4515c566-5748-443a-9832-98cc02762322.PNG">

-Invoices can be assigned individually or in bulk to selected flats.

<img width="956" alt="06 3" src="https://user-images.githubusercontent.com/71590181/164474997-ded03b67-e87d-4fc1-8a93-46d4e75efbaa.PNG">

<img width="955" alt="06 4" src="https://user-images.githubusercontent.com/71590181/164475008-b681fc1a-cb86-4fd2-a396-72a2b15b8f95.PNG">


- Payment status can be viewed in the “Genel Fatura Durumu” page. 

<img width="943" alt="07 1" src="https://user-images.githubusercontent.com/71590181/164478552-ffeb7a90-77e3-4713-b16f-69f97cadea98.PNG">

- “Borç Alacak Durumu” page shows overall financial status. 

<img width="949" alt="07 2" src="https://user-images.githubusercontent.com/71590181/164478617-b06d9661-d43f-4801-bcaf-9b544bd4fe15.PNG">


# My Account Section

- Available to all users regardless of role.
- Users can view invoices, make payments, and see payment history.

<img width="950" alt="8 1 " src="https://user-images.githubusercontent.com/71590181/164479624-9d54c7df-ee4c-4e65-874b-f00022c5a1ec.PNG">

<img width="956" alt="8-2" src="https://user-images.githubusercontent.com/71590181/164479692-9667a431-5861-4396-a96d-1867db182f9b.PNG">

- Password change functionality is available.

<img width="939" alt="9" src="https://user-images.githubusercontent.com/71590181/164479796-a249006f-0f1b-4da3-9686-c50de3dac9d6.PNG">


# Messaging

- Messaging section is accessible via the envelope icon at the bottom left.
- Real-time notifications are displayed when a message is received.

![m1](https://user-images.githubusercontent.com/71590181/164583168-1d2a042e-071b-47e4-943b-df6a8630d0fc.PNG)

- Users can see message notifications instantly.

![m2](https://user-images.githubusercontent.com/71590181/164583249-cb5e8389-922c-4fe3-9f0a-71399b2103e7.PNG)

-Users can see chat history and unread messages are highlighted.

![m4ı](https://user-images.githubusercontent.com/71590181/164583428-081f38be-7005-4e10-a2c6-5bb61864bc3e.PNG)

-Notifications disappear after reading messages.

![m6](https://user-images.githubusercontent.com/71590181/164583481-97416ccb-1467-4135-9c25-ce1aefdceb15.PNG)

-Users can search and add new contacts to start messaging.

![m8](https://user-images.githubusercontent.com/71590181/164583657-2063308c-2746-46ec-93c2-f00147285a45.PNG)

- Secure logout is available from the bottom menu.

