# DSA & CP Search Engine

A fast search engine for discovering Data Structures and Algorithms (DSA) and competitive programming problems across multiple coding platforms.

[![Live Demo](https://img.shields.io/badge/Live_Demo-Vercel-000000?logo=vercel)](https://dsa-cp-search-engine-two.vercel.app)
[![Backend API](https://img.shields.io/badge/API-Render-46E3B7?logo=render&logoColor=000000)](https://dsa-cp-search-engine-yrbx.onrender.com)
[![GitHub](https://img.shields.io/badge/GitHub-Biswajeet2004-181717?logo=github)](https://github.com/Biswajeet2004/DSA-CP-search-engine)

## Live links

- **Website:** [dsa-cp-search-engine-two.vercel.app](https://dsa-cp-search-engine-two.vercel.app)
- **Backend API:** [dsa-cp-search-engine-yrbx.onrender.com](https://dsa-cp-search-engine-yrbx.onrender.com)
- **Repository:** [github.com/Biswajeet2004/DSA-CP-search-engine](https://github.com/Biswajeet2004/DSA-CP-search-engine)

> The backend is hosted on Render's free tier. Its first request after a period of inactivity may take around 50 seconds or longer while the service wakes up.

## Features

- Search thousands of DSA and competitive programming problems from one interface
- Search by problem title, topic, tag, or keyword
- Results from LeetCode, Codeforces, CodeChef, AtCoder, and CSES
- Relevance-based results using TF-IDF and cosine similarity
- Direct links to the original problem pages
- Responsive, lightweight frontend

## Tech stack

- **Frontend:** HTML, CSS, and JavaScript
- **Backend:** Node.js and Express
- **Search:** Natural, TF-IDF, and cosine similarity
- **Data collection:** Puppeteer
- **Frontend hosting:** Vercel
- **Backend hosting:** Render

## Project structure

```text
DSA-CP-Search-Engine/
|-- Frontend/
|   |-- index.html
|   |-- styles.css
|   |-- script.js
|   `-- logos/
|-- Backend/
|   |-- index.js
|   |-- scrape.js
|   |-- merge.js
|   |-- corpus/
|   |-- problems/
|   |-- utils/
|   `-- package.json
`-- README.md
```

## Run locally

### Prerequisites

- [Node.js](https://nodejs.org/) and npm
- A local static-file server, such as the VS Code Live Server extension

### Start the backend

```bash
cd Backend
npm install
npm start
```

The API will be available at `http://localhost:3000`.

### Start the frontend

For local development, set the API URL at the top of `Frontend/script.js`:

```js
const API_BASE_URL = "http://localhost:3000";
```

Then serve the `Frontend` directory using Live Server or another static-file server. Do not open `index.html` directly with a `file://` URL because the backend's CORS configuration expects a local web-server origin.

## API

### Health check

```http
GET /
```

### Search for problems

```http
POST /search
Content-Type: application/json

{
  "query": "binary search"
}
```

The response contains up to 100 relevant problems:

```json
{
  "results": []
}
```

## Deployment

The frontend is deployed from the `Frontend` directory on Vercel. The backend is deployed from the `Backend` directory on Render.

The Render service uses the following configuration:

```text
Build command: npm install
Start command: npm start
Environment variable:
FRONTEND_URL=https://dsa-cp-search-engine-two.vercel.app
```

The production API URL is configured in `Frontend/script.js`.

## Author

**Biswajeet**

- GitHub: [@Biswajeet2004](https://github.com/Biswajeet2004)

## Acknowledgment

This repository is a personalized and deployed version of the original [DSA-CP-Search-Engine](https://github.com/devendraa-01/DSA-CP-Search-Engine) project by [Devendra Pratap Singh](https://github.com/devendraa-01). Credit for the original implementation and its earlier commit history belongs to the original author.

## Contributing

Suggestions, bug reports, and improvements are welcome. Open an issue or submit a pull request through the [GitHub repository](https://github.com/Biswajeet2004/DSA-CP-search-engine).
