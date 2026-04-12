# :mag: OpenVAS Vulnerbility Scanning

## 1. Install Docker:
  - In Terminal
    
    ***`brew install -cask docker`***

    - This downloads and installs docker desktop to applications

<img width="800" height="1000" alt="Install Docker" src="https://github.com/chosn12/Open-VAS-Vulnerbility-Scanning-/blob/3350834ed7740e3e9139eb990341fb5b5d69a5e8/screenshots/install%20docker.png"/>

## 2. Start Docker Desktop:
  - In Terminal

    ***`open /Applications/Docker.app`***

    - This will open docker desktop allowing it will run in the background
    - Docker must be running to use docker commands

<img width="800" height="1000" alt="Start Docker" src="https://github.com/chosn12/Open-VAS-Vulnerbility-Scanning-/blob/b97113b17e46060152c95fec6fddfa73d8ea08af/screenshots/start%20docker.png"/>

## 3. Verify Docker Installation:
  - In Terminal

    ***`docker --version`***

    ***`docker run hello-world`***

    - This will display the version of docker and message verifying the status of you installation


<img width="800" height="1000" alt="Docker version" src="https://github.com/chosn12/Open-VAS-Vulnerbility-Scanning-/blob/edd89bcd50ef71da515c264daefa00fdf172edf9/screenshots/docker%20version.png"/>

<img width="800" height="1000" alt="Hello World Docker" src="https://github.com/chosn12/Open-VAS-Vulnerbility-Scanning-/blob/648a9c19e0171943931a9c11ca72ac9b952a594a/screenshots/hello%20world-docker.png"/>


# :fireworks: Run OpenVAS

## :one: Clone the Offical Repo:
  - In Terminal

    ***`mkdir -p ~/greenbone-community-container && cd ~/greenbone-community-container`***
      - Creates a folder for the Repo and changes directory to the newly created folder  

    ***`curl -f -O -L https://greenbone.github.io/docs/latest/_static/docker-compose.yml`***
      - Download the Greenbone Repo to the newly created folder

    ***`docker compose -f docker-compose.yml up -d`***
      - Launches OpenVas by downloading images and starts the services running in the background
   
   <img width="800" height="1000" alt="Greenborn Repo" src="https://github.com/chosn12/Open-VAS-Vulnerbility-Scanning-/blob/70f56cbd30c8bc933148ea253a00bb8af014f1c2/screenshots/greenbone%20repo.png"/>


## :two: Login to OpenVAS:
  - Open a web browser
    ***`https://localhost`***
      - log in to the web interface of OpenVAS with admin and password and user name. Change the password after set up
   
   <img width="800" height="1000" alt="localhost" src="https://github.com/chosn12/Open-VAS-Vulnerbility-Scanning-/blob/e88da944550de544b9756b794f2c8cef9c04d905/screenshots/localhost.png"/>





## :three: How to Change the Password:
  - In Terminal
    ***`docker compose exec -u gvmd gvmd gvmd --user=admin --new-password='YourPasswordHere'`***
      

  <img width="800" height="1000" alt="Change Password" src="https://github.com/chosn12/Open-VAS-Vulnerbility-Scanning-/blob/16568232b6613d240cfe5a51583c7d3d5b80c520/screenshots/change%20password.png"/>



# Scanning Metasploitable2 VM

## :one: Log into OpenVas 
  - Type https://localhost in a web browser
  - Log in 
   

## :two: Start Scan
  - Click scan on the left sidebar
  - Select Tasks
  - Click the task wizard icon (wand)
      - Select Advanced Task Wizard
        -  Enter the task name
        -  Select Scan Configuration
        -  Enter Target Host IP Address (Metasploitable2)
  - Click Create

## :three: Retreive Report
  - Once the scan is complete
      - Click the date of the desired report

The report is arranged by categories tabs 


<img width="1000" height="1400" alt="Report" src="https://github.com/chosn12/Open-VAS-Vulnerbility-Scanning-/blob/039ee951ff8ad4f54ece6086238f84fdadd9158e/screenshots/Report.png"/>

# :x: Summary
  - Docker must be running to execute any docker commands
  - OpenVas can only be run from the folder containing the `docker-compose.yml` file
  - https://localhost is the secure site to log into OpenVAS
