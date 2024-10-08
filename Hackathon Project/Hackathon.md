# Hackathon Project: Music Library Manager

## Overview of the Project

Music Library Manager is a Flask-based web application I created to allow users to manage their music libraries effortlessly. The application enables users to edit metadata, upload tracks to an AWS S3 bucket, and perform bulk actions on their music collection. This project was inspired by the need for a simple yet powerful tool to manage personal music libraries, especially for users who prefer to have complete control over their music metadata.

### Purpose and Users

- **Users:** The primary users are music enthusiasts who want to organize their music collections efficiently and securely store them in the cloud.
- **Job:** The application provides a centralized platform where users can upload, edit, and manage their music tracks, ensuring their collections are always up to date with accurate metadata.
- **Inspiration:** I was inspired to build this application by my personal experience of managing a growing music library. I wanted a tool that could streamline the process of organizing tracks and make it easy to access my music from anywhere.
- **Key Features:** The most important features include user authentication, music upload to AWS S3, the ability to view, edit, and delete tracks, and bulk actions that allow users to manage multiple tracks simultaneously.

### STAR Interview Questions

- **Situation:** I created Music Library Manager as a solution for individuals who struggle with organizing and managing their digital music collections. The application addresses the need for a streamlined, cloud-based solution to keep music libraries organized and accessible.
- **Task:** Before building the application, I planned its structure carefully, focusing on a user-friendly interface and robust backend functionality. The design process involved outlining the core features, selecting the appropriate technologies, and mapping out the user flow from registration to managing music tracks.
- **Action:** I implemented the application using Flask for the backend, with user authentication and session management handled through Flask-Login. The music tracks are uploaded to an AWS S3 bucket, and metadata is managed using the eyed3 library. The bulk action functionality was developed to allow users to perform edits and deletions on multiple tracks in a single operation. One of the main challenges was integrating AWS S3 with Flask to securely handle the uploading and management of large music files, particularly ensuring that the uploads were reliable and efficiently processed.
- **Result:** The final application allows users to securely upload and manage their music tracks with ease. Key functionalities such as bulk editing and the ability to handle large libraries make it a powerful tool for any music lover. This project solidified my knowledge in Flask web development and enhanced my understanding of cloud storage integration, particularly in how to securely manage and deploy applications that involve user authentication and large file handling. The application has been deployed and can be accessed live [here](https://music-library-9r5k.onrender.com). 


<img width="650" alt="Music Library Manager Screenshot" src="https://github.com/user-attachments/assets/29e716c3-6ac3-42ec-a786-79b0d4bcd65f">

<img width="650" alt="Music Library Manager Screenshot S3" src="https://github.com/user-attachments/assets/2ace3c2c-67fd-4af1-96f2-757f3d26a92f">



## Technologies

- **Backend:** Flask 2.3
- **Frontend:** HTML5, CSS3, Bootstrap 5
- **Database:** SQLAlchemy with SQLite (for development)
- **Cloud Storage:** AWS S3
- **Authentication:** Flask-Login
- **Metadata Handling:** eyed3 0.9.7
- **Deployment:** Render.com

### Dependencies and Versions

- Python 3.8+
- Flask 2.3
- SQLAlchemy 2.0
- Flask-Login 0.6
- eyed3 0.9.7
- boto3 1.28
- Jinja2 3.1
- Werkzeug 2.3

### Deployment Tools

- Render.com for hosting the application
- AWS S3 for storing uploaded music tracks

## Competencies

### JF 1.6: Can follow software designs and functional/technical specifications

- **Situation:** While building the Music Library Manager, I followed specific design principles to ensure the application met the intended functionality and user experience.
- **Action:** I carefully implemented the technical specifications by structuring the application’s models, views, and controllers according to best practices. This included defining clear routes, implementing user authentication, and ensuring the seamless handling of music metadata.
- **Result:** The adherence to these design principles resulted in a functional and intuitive application that meets the users' needs for managing their music libraries efficiently.

### JF 3.4: Can create a logical and maintainable codebase

- **Situation:** The Music Library Manager required a well-structured codebase that would be easy to maintain and scale as new features were added.
- **Action:** I implemented best practices for code organization, including separating concerns across models, views, and templates in Flask. I also ensured that the code was thoroughly commented and that the logic was clear and concise.
- **Result:** The resulting codebase is logical and maintainable, making it easier for future developers (or myself) to understand and modify the application. The use of Flask and SQLAlchemy also supports the modular and scalable nature of the project.

### JF 4.3: Is able to build, manage, and deploy code into the relevant environment

- **Situation:** Deploying the Music Library Manager required careful consideration of the deployment environment to ensure that the application ran smoothly in production.
- **Action:** I used Render.com for deployment, configuring the necessary environment variables and ensuring that the AWS S3 integration was secure and efficient.
- **Result:** The application was successfully deployed and is accessible online, with a seamless deployment process that allows for easy updates and maintenance. The deployment configuration also ensures that the application is secure.
