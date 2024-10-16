### Explanation of Components

- **User**: The end-user of the app who sends an SOS during a disaster.

- **Load Balancer**: Distributes incoming requests efficiently across servers, ensuring high availability and reliability.

- **Web Server (Netlify)**: Hosts the main Flutter web application, providing a fast and scalable frontend experience.

- **Flutter Frontend**: The mobile and web application built using Flutter, which interacts with users and presents features like sending SOS alerts and viewing maps.

- **Mapbox**: Provides custom maps, incorporating historical data about frequently flooded areas and safe spots. Users can add new data points through the app.

- **Hetzner VM**: The virtual machine where the backend services are hosted.

  - **PostgreSQL Database**: Manages general database needs, such as user data and SOS requests.
  
  - **MongoDB**: Optimized for faster reads, useful for analytics and other quick-access data.
  
  - **ElasticSearch**: Handles powerful search capabilities, future AI features, and complex analytics.
  
  - **Docker**: Containerizes applications to ensure consistent deployment across environments.
  
  - **Portainer**: A management UI for Docker that helps monitor and manage containers.

- **CI/CD Pipeline**: Automates the deployment process.

  - **GitHub**: Hosts the codebase and triggers the CI/CD pipeline.
  
  - **Automated Build**: Compiles the application and runs tests.
  
  - **Deployment Targets**: Deploys to Netlify, Firebase Hosting, and Docker containers for backup.

- **Dispatcher**: The personnel who views the generated routes and receives notifications about SOS alerts.

- **Rescue Route Generator**: A component that calculates efficient routes for rescuers, leveraging data from ElasticSearch for quick access.

- **Rescue Teams**: The teams that respond to SOS alerts, notified by the dispatcher.

- **Firebase Authentication**: Manages user authentication and authorization for secure access to the application.
