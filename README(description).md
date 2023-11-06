# Week 5 HW: Video Hosting, Flask App and Cloud Deployment:

## 1. Video Creation:
- First found a video or a clip that I wanted to include into my flask app with the theme I had chosen.
- Went on Youtube, found an appropriate clip that was less than 60 sec, and also permitted downloads and downloaded in an mp4 format.
- After doing so the platform I chose was Azure so I logged in and prepared to upload the video and image I wanted to include in my flask app.

## 2. Cloud CDN & Uploading/Video Hosting:
- Went into Azure and created a resource group in which we can store everything for this app
    - Such as: CDN, container, webapp
      <img width="1000" alt="Screenshot 2023-11-05 at 5 54 52 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/a4a312d4-7d97-4f7c-9fa8-f4850c38a412">

- After creating the resource went ahead and created a CDN instance.
- Then we created an endpoint that ensured that access was granted to both blobs and other containers.
    <img width="500" alt="Screenshot 2023-11-05 at 8 48 10 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/a1929619-7561-46a6-822c-4d607203db26">

- Then we left a tab open on the endpoint we created, focusing on the endpoint hostname that will be used later on with the video and picture integration after the container is created.
  
    <img width="800" alt="Screenshot 2023-11-05 at 8 48 56 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/a222cafd-0ab6-4793-a059-edab044f7f67">

- Then we would click on the containers section in Azure in which we are going to create a new container instance and the storage account setup should look something like this:
  
<img width="900" alt="Screenshot 2023-11-05 at 8 51 34 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/8abd825d-1b63-49ff-85b6-513a49dbd266">

- Inside this storage account we navigated to Containers under Data Storage on the left menu tab, and created a container instance, allowing anonymous read access to containers and blobs:
  <img width="600" alt="Screenshot 2023-11-05 at 8 54 29 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/e6e7a941-b956-4690-bfa4-965f8e3e3d37">

- After creating the container we double-click on it and we are in a "dropbox" like platform format, in which we can upload the images or videos that we want to store and then later on include in our flask app: (in this case a picture and video was uploaded)
<img width="800" alt="Screenshot 2023-11-05 at 8 56 03 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/19f72688-0338-484f-8c9c-c9ed316d206d">

## 3. Creating the Flask App in this case in Google Shell:
- First, I navigated into the Google shell environment and cloned my repo that wanted to store my app and its data in.
- Then after doing so I created folders necessary for the setup of my Flask app such as ```requirements.txt``` file, a templates folder (in which I included my simple ```index.html``` folder that included all of my tailwind style codes for my apps format)
- In order to insert the video and the picture I wanted to include in the code inside my ```index.html``` file I had to create the url using Azure.
- I went back into Azure and navigated in the tab created before that had the CDN endpoint instance open with the endpoint hostname displayed and opened another tab with my container instance open and the video and image i had uploaded displayed
- From there I used the endpoint hostname and completed the URL with the end of the video's URL, and repeated that with the image as well, creating 2 new ones as shown below:
  <img width="1000" alt="Screenshot 2023-11-05 at 9 11 53 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/644bcbf1-8b22-461c-8a3a-ee3cd6a49e9c">

  <img width="1000" alt="Screenshot 2023-11-05 at 9 07 56 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/e4406698-13b0-448f-98eb-062266f6a27d">
  
- The result of both should look similar to the ones below included in the Flask app code:
  <img width="816" alt="Screenshot 2023-11-05 at 9 10 22 PM 1" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/247cc416-7984-4c29-b09b-4cc8418c3519">

- Then after making all the necessary folders and changes and after following the Tailwind official document of directions on their website, ensured that I could deploy it locally in the Google Shell Environment & that my preview in Tailwind Play also looked good:
[Screen Recording 2023-11-05 at 3.30.47 PM.zip](https://github.com/angeliki-tzanou/flask_5_tailwind/files/13261871/Screen.Recording.2023-11-05.at.3.30.47.PM.zip)

<img width="1000" alt="Screenshot 2023-11-05 at 3 30 08 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/9f27fe85-177c-4224-bcca-35413eb7dbe4">
<img width="1000" alt="Screenshot 2023-11-05 at 4 27 37 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/c434018d-05c1-4ccc-825a-8286a75ebd39">

## 4. Cloud Deployment: Azure
- First went into Google Shell and ensured that Azure was installed and could properly login
- In order to install in the google shell environment I used the following command ``` -sL https://aka.ms/InstallAzureCLIDeb | sudo bash```.
- Then after completing that step I ran in my terminal a simple ```az``` command to make sure it was installed properly
  <img width="600" alt="Screenshot 2023-11-05 at 4 40 33 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/5a207663-02ea-4b32-a433-ac7dbb84bdcd">

- Then I used the following command in order to login and link my environment to my Azure ```az login --use-device-code``` . A message of authentication popped up and chose the account I wanted to use. It was successfully linked since the message below appeared:
  
  <img width="300" alt="Screenshot 2023-11-05 at 5 36 24 PM" src="https://github.com/angeliki-tzanou/flask_5_tailwind/assets/141374140/b87a3aec-bbe8-4843-8ae9-c6ab53c162b0">





