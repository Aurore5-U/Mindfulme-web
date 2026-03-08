# MindCare App

**MindCare** is a simple Flask-based web application designed to help users track and manage their mental health. This app runs inside a Docker container for easy deployment.

## 🌐 Live Deployed App

> **Your app is deployed at:**
> ### 👉 https://mindcare-app.onrender.com

If the link above doesn't open correctly, follow these steps to find your exact URL:

1. Go to [https://dashboard.render.com](https://dashboard.render.com) and sign in
2. Click on the **mindcare-app** service in your dashboard
3. The URL is shown at the top of the service page (e.g. `https://mindcare-app.onrender.com`)

---

## Features

* User-friendly interface for mental health check-ins
* RESTful API powered by Flask
* Runs inside a Docker container for easy portability

## Getting Started

### Prerequisites

* Docker installed on your machine
* Basic understanding of Docker commands

### Running the app locally with Docker

1. Clone the repository:

   ```bash
   git clone https://github.com/Aurore5-U/playing_with_API.git
   cd playing_with_API
   ```

2. Build the Docker image:

   ```bash
   docker build -t mindcare-app .
   ```

3. Run the container (maps container port 8080 to host port 5000):

   ```bash
   docker run -d -p 5000:8080 --name mindcare-container mindcare-app
   ```

4. Open your browser and go to:

   ```
   http://localhost:5000
   ```

## Deploying to the cloud (Render.com)

This repository includes a `render.yaml` configuration and a GitHub Actions workflow for automatic deployment to [Render.com](https://render.com) (free tier).

### First-time setup

1. Create a free account at [https://render.com](https://render.com)
2. Click **New → Web Service** and connect your GitHub repository
3. Render will detect the `render.yaml` file automatically and configure the service
4. Once deployed, your URL will be shown in the Render dashboard as:
   ```
   https://mindcare-app.onrender.com
   ```
5. Copy the URL from the Render dashboard and share it!

### Automatic deployments

After setup, every push to the `main` branch will automatically trigger a new deployment. You can follow the progress and see the live URL in:
- The GitHub Actions tab of this repository
- Your [Render dashboard](https://dashboard.render.com)

## Stopping the app

```bash
docker stop mindcare-container
docker rm mindcare-container
```

## Troubleshooting

* If you get errors about the container name already in use, run:

  ```bash
  docker rm -f mindcare-container
  ```
* Ensure Docker daemon is running.
## creator's note
i wanted to create a user friednly which had a front-end and a backend but the time have not been my friend i may call this as my prototype but promise you to implement my idea in the times to come and i wish you to consider the thought and the work and evrything 
Thank you
## License

This project is open source and available under the MIT License.

---

