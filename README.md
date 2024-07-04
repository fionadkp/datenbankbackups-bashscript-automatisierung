
# Database Backups Bash Script Automation

This repository contains a bash script for automating database backups using Docker and MariaDB.

```
MADE BY BERKE AND FIONA
```

## LINUX

### Build Docker Image

To build the Docker image, run the following command:

```
sudo docker build -t mariadb .
```

### Run Docker Container

To run the Docker container with MariaDB, execute the following command:

```
sudo docker run --name mariadb -e MYSQL_ROOT_PASSWORD=root -d -p 3306:3306 mariadb
```

Make sure to replace `root` with your desired password for the MySQL root user.

Once the container is running, you can access the MariaDB database on `localhost:3306`.

### Change File Permissions

To change the file permissions of `connection_backup.sh` and make it executable, run the following command:

```
chmod +x connection_backup.sh
```

### Run the Script

To run the `connection_backup.sh` script on Linux, execute the following command:

```
./connection_backup.sh
```

Make sure you are in the same directory as the script before running the command.


## WINDOWS

### Build Docker Image

To build the Docker image on Windows, run the following command:

```
docker build -t mariadb .
```

### Run Docker Container

To run the Docker container with MariaDB on Windows, execute the following command:

```
docker run --name mariadb -e MYSQL_ROOT_PASSWORD=root -d -p 3306:3306 mariadb
```

Make sure to replace `root` with your desired password for the MySQL root user.

Once the container is running, you can access the MariaDB database on `localhost:3306`.

### Run the Script on Windows with WSL Terminal

To run the `connection_backup.sh` script on Windows using the Ubuntu WSL 2 terminal, follow these steps:

1. Open the Ubuntu WSL 2 terminal.

2. Navigate to the directory where the script is located. For example, if the script is located in `/home/berke-poslu/Code/vscode/Datenbankbackups-bashscript-automatisierung`, you can use the following command:

    ```
    cd /home/berke-poslu/Code/vscode/Datenbankbackups-bashscript-automatisierung
    ```

3. Make sure the script has executable permissions. If not, run the following command to change the file permissions:

    ```
    chmod +x connection_backup.sh
    ```

4. Run the script by executing the following command:

    ```
    ./connection_backup.sh
    ```

    This will execute the `connection_backup.sh` script and start the database backup process.

Make sure you have Docker and MariaDB installed and properly configured in your Ubuntu WSL 2 environment before running the script.

