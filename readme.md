<a id="readme-top"></a>
# Python Django :star:
___
A django app for helping school admin to manage information about the colleges, organization, and students efficiently through the website.

### List of features 
* **Display information** about the college, organization, and students.
* Allows **adding, modifying and deleting.**
* **Search and Filters** for easy access for needed information.  
* Account Authentication.
* Authentication with Google and Github account.

### Project Structure
```
docker_PSUSphere/
├── projectsite/              ← Django source code
│   ├── Dockerfile            ← Multi-stage image definition
│   ├── docker-compose.yml    ← Compose file for development
│   ├── .dockerignore         ← Files excluded from the image
│   ├── requirements.txt      ← Python dependencies
│   ├── manage.py
│   ├── projectsite/          ← Django settings, URLs, WSGI
│   └── studentorg/           ← Main app (models, views, forms)
└── for_client/
    └── docker-compose.client.yml  ← One-file deploy (image only)
```

### Set-up Docker
Requirements:
Check if docker is installed.

Enter the command in Terminal/Command Prompt/Powershell
```
C: ...> docker --version 
```
Desired Result
```
C: ...> Docker version 29.5.3, build d1c06ef
```
> *if not, Follow the Installation Guide*

<p align="right">(<a href="#readme-image">Skip to get image</a>)</p>


#### Important Requirements!

If not installed, install Docker:
• Windows/Mac: Download Docker Desktop from docker.com
• Linux: sudo apt-get install docker.io

> Signup to https://hub.docker.com/signup

#### How to Download and Install Docker Desktop?
Download and install Docker Desktop for Windows.
> Visit Docker's website: https://www.docker.com/products/docker-desktop

> Click "Download for Windows"


1. If prompted during installation or on the first launch to enable or update WSL 2, click Yes or Install.

2. Restart the computer if the installer asks you to.

3. Open your terminal, navigate to the for_client folder, and run.

```
cd C:To\Your\Directory\docker_PSUSphere\for_client
```
```
docker compose up -d
```
```
docker_PSUSphere/
├── projectsite/  
│   └── (Other folders)
└── for_client/
    └── docker-compose.client.yml
```

Check if docker is succesfull installed with: 
``` 
docker --version
``` 

<a id="readme-image"></a>

__Pull the image__
```
docker pull micro7/my-app:latest
```

1. Pull new version
```
docker-compose pull
```
Expected Result (Example)
>*latest: Pulling from micro7/my-django
abc123: Pull complete
def456: Pull complete
Status: Downloaded newer image for micro7/my-django:latest*

#### Run the Application
Start the application: 
```
docker-compose up -d
```
Expected output:
>Creating network "psusphere_default" with the default driver
Creating psusphere_web_1 ... done
Attaching to psusphere_web_1
web_1 | Performing system checks...
web_1 | System check identified no issues (0 silenced).
web_1 | Starting development server at http://0.0.0.0:8000/

Check if running: 
```
docker-compose ps
```
View logs: 
```
docker-compose logs -f web
```
Access the app: Open browser: http://localhost:8000

Step 4: Initial Setup (Once Time Only)
Create superuser:
```
docker-compose exec web python manage.py createsuperuser
```
Run any additional commands

```
docker-compose exec web python manage.py collectstatic –-noinput
```

### Author

<div align='left'>
    <img alt="Profile Image" src="https://avatars.githubusercontent.com/u/206431058?s=400&u=315f6b05ac5ecf37c464dd8d144907c1ecac9056&v=4" width="50px" border-radius="50%">  
</div>
<strong>JuliusMarckArnesto</strong> 
    
* <a href="julius.arnesto.1110@gmail.com">julius.arnesto.1110@gmail.com</a>
* [github.com/JuliusMarckArnesto](https://github.com/JuliusMarckArnesto)
<p align="right">(<a href="#readme-top">Back to top</a>)</p>

#### References
Docker Guide: [Visit Here](https://drive.google.com/file/d/1lmgDEIqAWf7kEzRQBOe55_-6Mgf7GMoC/view?usp=sharing)