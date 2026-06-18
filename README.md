
# Python Flask Application

## Project Overview

This project is a simple Python Flask web application that demonstrates web application development and deployment fundamentals. The application is designed to run locally as well as on a production server using Nginx and Gunicorn.

### Objectives

* Build a web application using Flask.
* Understand application deployment on Linux servers.
* Learn web server integration with Nginx and Gunicorn.
* Practice DevOps deployment workflows.

---

## Architecture

```text
User Browser
      │
      ▼
    Nginx
      │
      ▼
   Gunicorn
      │
      ▼
 Flask Application
```

### Components

* **Flask**: Python web framework for building the application.
* **Gunicorn**: WSGI server for running Flask in production.
* **Nginx**: Reverse proxy server handling incoming requests.
* **Linux Server**: Hosts the application.

---

## Prerequisites

Before running the project, ensure the following are installed:

* Python 3.x
* pip
* Git
* Flask
* Gunicorn (for production)
* Nginx (for production deployment)

Verify installation:

```bash
python3 --version
pip3 --version
git --version
```

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/satyaprakash196/Python-Flask.git
cd Python-Flask
```

### Create Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run Locally

Start the Flask application:

```bash
python app.py
```

Open your browser and visit:

```text
http://localhost:5000
```

---

## Deployment Steps

### Step 1: Launch EC2 Instance

* Create an Ubuntu EC2 instance.
* Allow ports:

  * 22 (SSH)
  * 80 (HTTP)
  * 443 (HTTPS)

### Step 2: Install Required Packages

```bash
sudo apt update
sudo apt install python3-pip python3-venv nginx -y
```

### Step 3: Clone Repository

```bash
git clone https://github.com/satyaprakash196/Python-Flask.git
cd Python-Flask
```

### Step 4: Configure Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Step 5: Install Gunicorn

```bash
pip install gunicorn
```

Run:

```bash
gunicorn --bind 0.0.0.0:8000 app:app
```

### Step 6: Configure Nginx

Create an Nginx configuration file and proxy requests to Gunicorn.

Restart Nginx:

```bash
sudo systemctl restart nginx
```

### Step 7: Access Application

Open:

```text
http://YOUR_PUBLIC_IP
```

---

## Screenshots

Add screenshots inside a folder named:

```text
screenshots/
```

Example:

```text
screenshots/
├── home-page.png
├── deployment-success.png
└── ec2-instance.png
```

### Application Home Page

(Add screenshot here)

### Deployment Verification

(Add screenshot here)

---

## Project Structure

```text
Python-Flask/
│
├── app.py
├── requirements.txt
├── templates/
├── static/
├── screenshots/
├── README.md
└── .gitignore
```

---

## Future Improvements

* Dockerize the application.
* Deploy using Kubernetes.
* Implement CI/CD using GitHub Actions.
* Add HTTPS using SSL certificates.
* Integrate monitoring with Prometheus and Grafana.
* Store application logs centrally.
* Deploy infrastructure using Terraform.

---

## Author

Satya Prakash

GitHub: https://github.com/satyaprakash196

Learning DevOps | AWS | Linux | Docker | Kubernetes | Terraform | Jenkins
