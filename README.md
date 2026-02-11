# test-laravel-setup
Reference repository for setting up a React + Laravel based Application with a MySQL Database.

## Prerequisites
- Check for PHP and Composer Installation: 
```console
php -v
composer -v
```
- If any of the following have not been installed:
```console
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://php.new/install/windows/8.4'))
```

## Create an Application via Starter Kit
```console
laravel new test-app
```
- <ins>Configurations:</ins>
  <br>
  <br>
  1. What starter kit would you like to install?
     <br>
     **none**
     <br>
     <br>
  2. Which testing framwork do you prefer?
     <br>
     **0 (for Pest)**
     <br>
     <br>
  3. Do you want to install Laravel Boost to improve AI assisted coding?
     <br>
     **no**
     <br>
     <br>
  4. Which database will your application use?
     <br>
     **mysql (for MySQL)**
     <br>
     <br>
  5. Default database updated. Would you like to run the default database migrations?
     <br>
     **no**
     <br>
     <br>
  6. Would you like to run npm install and npm run build?
     <br>
     **yes**
     <br>
     <br>

## Installing Laravel Breeze
1. Enter your Project Folder:
```console
cd test-app
```
2. Run the following commands:
```console
composer require laravel/breeze --dev
php artisan breeze:install
```
The first line installs the Breeze Package whilst the second line runs the Breeze Installer.
<br>
<br>
Following the Breeze Installer, for the Breeze Stack select the **React with Inertia** option, **none** for optional features, and 0 again for the **Pest** Testing Framework.


## Connecting to your PostgreSQL Database
From the root folder of your application you will find a **.env** file.
<br>
<br>
Open and edit the the DB portion to match your database credentials:
```console
DB_CONNECTION=mysql
DB_HOST=<YOUR_DB_IP_ADDRESS>
DB_PORT=3306
DB_DATABASE=<YOUR_DB_NAME>
DB_USERNAME=root
DB_PASSWORD=<YOUR_DB_PASSWORD>
```
Afterwards, run the following command for database migrations:
```console
php artisan migrate
```

## Running your Development Servers
To check if the application is running we will run two separate terminals, one for the Backend and another for the Frontend. Both will run the same application view once accessible.

<ins>Backend:</ins>
```console
php artisan serve
```

<ins>Frontend:</ins>
```console
npm run dev
```
