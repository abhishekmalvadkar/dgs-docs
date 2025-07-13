# TDD-2 : Setup Predefined Users and Roles

## Problem Context

In DGS system we will have some predefined users and roles like below

Predefined users:
* System

Predefined roles:
* Admin
  * Responsible to manager everything along with users and organizations
* Manager
  * Responsible to manager projects, contexts and terms along with user assignment to project
* Member
  * Responsible to view terms and contexts related to assigned projects
* System
  * Responsible to send email notification and other automated tasks

We need to setup these users and roles in DGS database and also provide required  
support in DGS API Container.

Need to write tests as well to check that implemented solution is working as  
expected or not ?

## Database changes

### Create below tables

#### `users` Table

| Column            | Data Type   | Constraints                        |
| ----------------- | ----------- | ---------------------------------- |
| `id`              | VARCHAR(45) | Primary Key                        |
| `name`            | VARCHAR(50) | NOT NULL                           |
| `email`           | VARCHAR(50) | NOT NULL, UNIQUE                   |
| `last_login_time` | DATETIME    | Nullable                           |
| `active`          | BIT(1)      | NOT NULL, DEFAULT 1                |
| `role_id`         | VARCHAR(45) | NOT NULL, Foreign Key → `roles.id` |
| `created_by`      | VARCHAR(45) | Nullable, Foreign Key → `users.id` |
| `created_on`      | DATETIME    | Nullable                           |
| `updated_by`      | VARCHAR(45) | Nullable, Foreign Key → `users.id` |
| `updated_on`      | DATETIME    | Nullable                           |
| `delete_flag`     | BIT(1)      | DEFAULT 0                          |

---

#### `roles` Table

| Column        | Data Type    | Constraints      |
| ------------- |--------------| ---------------- |
| `id`          | VARCHAR(45)  | Primary Key      |
| `name`        | VARCHAR(50)  | NOT NULL, UNIQUE |
| `description` | VARCHAR(255) | Nullable         |

---

#### Create below INSERT Statements

* Insert Admin, Manager, System and Member roles into roles table (**Check Predefined roles section for description**)
* Insert System user with System role in users table
* Use [ULID Generator](https://it-tools.tech/ulid-generator) to generate ULID for above INSERT statements
* Keep them in liquibase section of dgs-service-api container

## Backend Changes

### Service: dgs-service-api

* Create required JPA entities (RoleEntity, UserEntity)
* Create BaseEntity to re-use common JPA entity properties
* Create required Spring Data JPA repositories (RoleRepo, UserRepo)
* Write DataJpaTest (Slice Test) to check inserted predefined users and roles are inserted properly in DGS database or not

### Final Thoughts

Learn during implementation, don't implement for the sac of implementation only






