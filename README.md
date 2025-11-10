# Campus Event Management Website

## Project Overview

This is a static website developed collaboratively by the **UCP DevOps Team** as part of the DevOps assignment.  
The website allows departments to showcase upcoming events, seminars, and workshops on campus. It contains **five interlinked pages**:

| Page         | Description                                | Assigned To |
| ------------ | ------------------------------------------ | ----------- |
| index.html   | Home page: event categories & navigation   | Team Lead   |
| about.html   | About the university and team              | Member 1    |
| events.html  | Lists 3–5 sample events with dates/details | Member 2    |
| gallery.html | Gallery of past events                     | Member 3    |
| contact.html | Contact form & social media links          | Member 4    |

All pages share a common **layout and styling** defined in `styles/style.css`.

---

## Project Structure

```

campus-events/
├── src/               # HTML source files
├── styles/            # CSS styles
├── .gitignore
├── .dockerignore
├── Dockerfile         # Shared Dockerfile for building images
├── package.json
├── README.md

```

> The `dist/` folder is generated automatically by Parcel and should **not** be committed.

---

## Setup & Installation

### Using Parcel (local development)

1. Install Parcel globally (if not already installed):

```

npm install -g parcel

```

2. Install dependencies:

```

npm install

```

3. Run development server:

```

npm start

```

4. Open your browser at [http://localhost:1234](http://localhost:1234)

5. Build the project for production:

```

npm run build

```

---

### Using Docker

1. Build the Docker image:

```

docker image build -t campus-events:1.0 .

```

2. Run the container locally:

```

docker run -d -p 2222:80 campus-events:1.0

```

3. Open your browser at [http://localhost:2222](http://localhost:2222)

4. Tag and push your image to Docker Hub:

```

docker image tag campus-events:1.0 <dockerhub-username>/campus-events:1.0
docker push <dockerhub-username>/campus-events:1.0

```

> Team members should use the same Dockerfile to build and push their own images.

---

## Team Workflow

-   **Main branch**: Protected; only Team Lead can merge.
-   **Develop branch**: Feature branches are merged here after review.
-   Each member works on their **assigned page** in a feature branch.
-   Pull Requests require **2 approvals for develop**, **3 approvals for main**.

---

## Team Members

| Name             | GitHub Username | Role      | Branch/Feature | Docker Image Name              |
| ---------------- | --------------- | --------- | -------------- | ------------------------------ |
| Abdullah Amir    | L1F22BSSE0245   | Team Lead | Main, index    | `<username>/campus-events:1.0` |
| Aziz Subhani     | Aziz49759       | Member    | About          | `<username>/campus-events:1.0` |
| Dalawar Ali      | DalawarAli9     | Member    | Events         | `<username>/campus-events:1.0` |
| Muhammad Touseef | M-Touseef       | Member    | Gallery        | `<username>/campus-events:1.0` |
| Talal Saleem     | TalalSaleem0075 | Member    | Contact        | `<username>/campus-events:1.0` |

---

## Notes

-   `.gitignore` excludes `node_modules` and `dist` for a clean repository.
-   `.dockerignore` excludes unnecessary files to keep Docker image small.
-   All members must build the project locally before creating Docker images.
-   Final submission by Team Lead includes consolidated Docker image and completed Table 1.
