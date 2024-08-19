# Frontend Project: React Notes App

## Overview of the Project

The React Notes App is a web application I developed to help users manage their notes and to-do items efficiently. The app supports adding, editing, deleting, tagging, and searching notes, with the additional feature of integrating OpenAI's capabilities for summarizing notes and generating new content based on user prompts. The application leverages React Context for state management and uses local storage to ensure that users' data persists across sessions.

### Purpose and Users

- **Users:** The target users are individuals looking to organize their daily tasks and notes in a simple, user-friendly interface.
- **Job:** The app serves as a personal note-taking tool that not only allows users to keep track of their thoughts and tasks but also enhances productivity with AI-driven features like note summarization and generation.
- **Inspiration:** I was inspired to create this app to address the need for a straightforward yet powerful note-taking solution that integrates modern AI capabilities, helping users manage their notes more effectively.
- **Key Features:** Key features include note management (add, edit, delete), searching and filtering notes by text and color, AI integration for note summarization and generation, and a dark mode toggle for a better user experience.

### STAR Interview Questions

- **Situation:** I created the React Notes App as a solution for individuals who need a versatile and efficient tool to manage their notes and tasks. The application also explores the integration of AI for enhancing note-taking processes.
- **Task:** Before diving into the development, I outlined the app's key functionalities, such as state management using React Context, persistent data storage with local storage, and AI-powered features using OpenAI's API. The design process involved setting up the project component structure and integrating Bootstrap for styling along with some custom CSS.
- **Action:** I developed the application using React and managed the global state with React Context. The AI integration was achieved by connecting to OpenAI's API, enabling features like note summarization and generation. Additionally, I implemented a dark mode feature and ensured the app's responsiveness and accessibility across different devices.
- **Result:** The final application allows users to manage their notes efficiently while benefiting from AI-powered features. The app's clean interface, combined with its advanced capabilities, provides an enhanced note-taking experience. The application is ready to be deployed and used as a daily productivity tool.


<img width="650" alt="React Notes App Screenshot" src="https://github.com/user-attachments/assets/11647d79-fce7-45bf-8ce0-891e61644222">
<img width="650" alt="React Notes App Screenshot" src="https://github.com/user-attachments/assets/160c0b19-9dcd-4bb4-b3e6-9e761a407ffa">


## Technologies

- **Frontend:** React 18.2.0, React Bootstrap 2.10.2
- **State Management:** React Context API
- **Routing:** React Router DOM 6.23.1
- **CSS Framework:** Bootstrap 5.3.3
- **AI Integration:** OpenAI API
- **Deployment:** Vite (development server)

### Dependencies

- `axios ^1.6.8`
- `bootstrap ^5.3.3`
- `react ^18.2.0`
- `react-bootstrap ^2.10.2`
- `react-dom ^18.2.0`
- `react-router-bootstrap ^0.26.2`
- `react-router-dom ^6.23.1`

### Deployment Tools

- Vite for running the development server and building the app.

## Competencies

### JF 2.7: Effectively manages state for complex User Interfaces

- **Situation:** The React Notes App required managing state across multiple components, especially when handling dark mode settings, notes, and AI-generated content.
- **Action:** I utilized the React Context API to manage global state, ensuring that components had access to necessary data and actions. I also implemented local storage for persisting state across sessions, ensuring user data was preserved even after the browser was closed.
- **Result:** The application manages state efficiently, providing a seamless user experience with instant updates across components when data changes. The use of React Context and local storage ensures that the app is both scalable and reliable. This project solidified my knowledge in using React Context for state management and reinforced my understanding of design principles for creating responsive and user-friendly interfaces.

### JF 2.5: Can implement a responsive User Interface

- **Situation:** It was essential that the React Notes App be accessible and user-friendly across different devices and screen sizes.
- **Action:** I used Bootstrap for responsive design and ensured that the layout was adaptable to various screen sizes. I also implemented a dark mode feature, allowing users to switch between themes based on their preference.
- **Result:** The app's user interface is fully responsive, providing a consistent and pleasant experience on desktops, tablets, and mobile devices. The dark mode feature enhances usability in low-light environments.

### JF 3.6: Can implement a RESTful API

- **Situation:** The AI integration in the React Notes App required interaction with OpenAI’s RESTful API to provide note summarization and generation features.
- **Action:** I integrated OpenAI's API using Axios to handle HTTP requests, enabling the app to send prompts and receive generated content or summaries in real-time.
- **Result:** The successful integration of the OpenAI API allows users to enhance their note-taking process with AI-generated content, providing additional value and functionality within the application.
