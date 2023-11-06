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
