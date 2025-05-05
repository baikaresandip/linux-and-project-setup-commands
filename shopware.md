# Shopware

# 📘 Shopware Important CLI Commands

This document lists commonly used Shopware CLI commands with detailed descriptions. These commands are executed from the root directory of a Shopware installation using the `bin/console` tool.

---

## 🔧 System & Maintenance

### `bin/console system:install`

Installs the Shopware system (creates schema, sets up admin user, etc.).

### `bin/console system:setup`

Interactive tool for configuring the `.env` file with database and app settings.

### `bin/console system:check`

Checks your system for Shopware requirements and readiness.

---

## 👤 User Management

### `bin/console user:create`

Creates a new Shopware admin user via prompts.

### `bin/console user:change-password`

Changes the password for an existing admin user.

###  `bin/console user:list`             

List current users

---

## 🔄 Cache & Indexing

### `bin/console cache:clear`

Clears all caches.

### `bin/console dal:refresh:index`

Refreshes and rebuilds the Doctrine abstraction layer (DAL) indexes.

### `bin/console dal:validate:entity`

Validates entity definitions.

---

## 🧱 Database & Migrations

### `bin/console database:migrate`

Applies pending core migrations to the database.

### `bin/console database:migrate-destructive`

Applies destructive database changes.

### `bin/console database:import`

Imports a raw SQL dump.

---

## 🧪 Testing & Debugging

### `bin/console debug:container`

Inspect available services in the DI container.

### `bin/console debug:event-dispatcher`

Displays event listeners and subscriber mappings.

### `bin/console debug:router`

Shows available routes and their configurations.

### `bin/console debug:autowiring`        

List classes/interfaces you can use for autowiring

### `bin/console debug:business-events`   

Dumps all business events

### `bin/console  debug:config`            

Dump the current configuration for an extension

### `bin/console debug:container`         

Display current services for an application

### `bin/console debug:dotenv`

List all dotenv files with variables and values

### `bin/console debug:event-dispatcher`  

Display configured listeners for an application

### `bin/console debug:messenger`         

List messages you can dispatch using the message buses


### `bin/console debug:router`            

Display current routes for an application

### `bin/console debug:scheduler `         

List schedules and their recurring messages


### `bin/console debug:serializer`        

Display serialization information for classes

### `bin/console debug:translation`       

Display translation messages information

### `bin/console debug:twig`              

Show a list of twig functions, filters, globals and tests

### `bin/console debug:validator`         

Display validation constraints for classes


---

## 📦 Plugins

### `bin/console plugin:list`

Lists all installed plugins.

### `bin/console plugin:install <plugin>`

Installs a plugin.

### `bin/console plugin:activate <plugin>`

Activates a plugin.

### `bin/console plugin:deactivate <plugin>`

Deactivates a plugin.

### `bin/console plugin:uninstall <plugin>`

Uninstalls a plugin.

### `bin/console plugin:update <plugin>`

Updates a specific plugin.

---

## 🌍 Administration

### `bin/console admin:create`

Legacy command to create admin users (use `user:create` now).

### `bin/console theme:compile`

Compiles storefront themes (CSS/JS).

---

## 🛒 Storefront & Build Tools

### `bin/console storefront:build`

Runs the complete asset build (npm + production build).

### `bin/console storefront:hot`

Starts a hot-reload dev server (requires frontend dependencies installed).

### `bin/console asset:install`

Installs symbolic links for assets.

---

## 📊 Elasticsearch

### `bin/console es:index`

Indexes data into Elasticsearch.

### `bin/console es:reset`

Deletes and recreates Elasticsearch indices.

---

## 🧰 Miscellaneous

### `bin/console scheduled-task:run`

Manually run scheduled background tasks.

### `bin/console messenger:consume`

Consumes messages from the message bus (queues).

### `bin/console theme:refresh`

Rebuilds the theme configuration.

### `bin/console framework:demodata`

Generates demo data for testing (optional).

---

For all commands, you can append `--help` to see options, e.g.:

```bash
bin/console plugin:install --help
```

---

📌 **Tip:** Always clear cache and rebuild theme after installing or updating plugins:

```bash
bin/console cache:clear && bin/console theme:compile && bin/console dal:refresh:index
```
