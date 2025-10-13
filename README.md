
# 🌐 Ponto Local - Infrastructure

## Required tools

- **Docker**: A platform to create and manage containers, essential for running the services in isolated environments.  
  [https://www.docker.com](https://www.docker.com)

## Running locally

Clone the repository

```bash
    git clone https://github.com/pontolocal/infrastructure.git
```

Enter the newly cloned folder:

```bash
    cd infrastructure
```
Run the following command to start the containers

```bash
    sudo docker compose up
```

By default, the services run on the following ports:

- backend: 8080  
- database: 5432  
- pgadmin: 5050  

And use the following configurations:

- database  
    - User: admin
    - Password: admin
    - Database Name: ponto_local
- pgadmin
    - User: admin@admin.com
    - Password: admin
 
You can change the ports and configurations through the `.env` file.

## Environment Variables Configuration

This file contains the environment variables needed to configure the backend service, database, and pgAdmin.

### Backend

- `BACKEND_PORT`: The port on which the backend service will run.  
  Default: `8080`

### Database

- `DATABASE_NAME`: The name of the database to use.  
  Default: `ponto_local`

- `DATABASE_USERNAME`: The username for connecting to the database.  
  Default: `admin`

- `DATABASE_PASSWORD`: The password for the database user.  
  Default: `admin`

- `DATABASE_HOST`: The hostname or container name of the database service.  
  Default: `database`

- `DATABASE_PORT`: The port on which the database service is listening.  
  Default: `5432`

### pgAdmin

- `PGADMIN_PORT`: The port on which the pgAdmin web interface will run.  
  Default: `5050`

- `PGADMIN_EMAIL`: The login email for pgAdmin.  
  Default: `admin@admin.com`

- `PGADMIN_PASSWORD`: The password for the pgAdmin login.  
  Default: `admin`

---

Make sure to update this file with the correct values before starting the services.
