# CSV-Visualizer: A Serverless, Client-Side Data Visualization PWA

## Overview

CSV-Visualizer is a high-performance, single-page application that provides instant data visualization from CSV files. It operates entirely on the client-side, making it a powerful tool for rapid analysis without data privacy compromises or server-side dependencies. The architecture is intentionally serverless, ensuring zero latency from network requests post-load and complete data security, as no user data is ever transmitted.

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Pull Requests](https://img.shields.io/badge/PRs-welcome-orange.svg)
![Tech Stack](https://img.shields.io/badge/tech-Vanilla_JS_|_HTML5_|_CSS3-yellow)

---

## Live Demonstration

( Will be added, once the project is completed. ) 

---

## Architectural Highlights & Core Features

This project is engineered with a focus on performance, security, and modern development practices.

* **Serverless Architecture**: By design, the application is a Progressive Web App (PWA) that can be hosted on any static file server (e.g., GitHub Pages, Vercel). This eliminates the need for backend infrastructure, reducing complexity and cost to zero.
* **Data Privacy by Default**: All file parsing and data processing occur within the browser's sandbox. No user-uploaded data ever leaves the client machine, making it suitable for sensitive information.
* **High-Throughput Parsing**: Leverages the multi-threaded capabilities of **Papa Parse** for efficient, in-browser parsing of CSV files, capable of handling large datasets without freezing the UI thread.
* **Reactive UI with Vanilla JS**: The interface is built without a heavy framework, demonstrating mastery of core JavaScript (ES6+). The UI reacts to user input, dynamically populating selection dropdowns based on the parsed CSV headers.
* **Interactive Data Rendering**: Utilizes **Chart.js** for rendering beautiful, interactive, and responsive charts on an HTML5 `<canvas>` element, optimized for performance.
* **Robust Error Handling**: Provides clear, contextual feedback for malformed CSVs, empty files, or data type mismatches.

---

## Technology Stack

| Category      | Technology / Library                                       | Purpose                                            |
| :------------ | :--------------------------------------------------------- | :------------------------------------------------- |
| **Core** | HTML5, CSS3, Vanilla JavaScript (ES6+)                     | Foundation of the web application.                 |
| **Rendering** | [Chart.js](https://www.chartjs.org/)                       | For interactive and responsive chart generation.   |
| **Parsing** | [Papa Parse](https://www.papaparse.com/)                   | For fast and reliable client-side CSV parsing.     |
| **Styling** | Flexbox, CSS Grid, CSS Custom Properties                   | For a modern, maintainable, and responsive layout. |
| **DevOps** | Git, GitHub                                                | Version control and code repository.               |

---

## Local Development Setup

No build tools or dependencies are required for this project.

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/csv-visualizer.git](https://github.com/your-username/csv-visualizer.git)
    ```

2.  **Navigate to the project directory:**
    ```sh
    cd csv-visualizer
    ```

3.  **Serve `index.html`:**
    Open `index.html` directly in a web browser, or use a lightweight server for a better development experience.
    ```sh
    # If you have Python 3 installed
    python3 -m http.server

    # Or use the Live Server extension in VS Code
    ```

---

## Input Data Specification

The application expects a well-formed CSV with the following constraints:

* The first row **must** be a header row containing column titles.
* Header names should be unique.
* Data must be comma-delimited.
* For quantitative charts (Line, Bar, Scatter), the column selected for the Y-Axis should contain valid numerical data. The `dynamicTyping` feature in Papa Parse will handle type inference.

---

## Contribution

Contributions and improvements are welcome. To maintain code quality, please ensure any submissions are formatted using Prettier and adhere to the existing architectural patterns.

1.  Fork the repository.
2.  Create a new feature branch (`git checkout -b feature/your-feature-name`).
3.  Commit your changes (`git commit -m 'feat: Add some feature'`).
4.  Push to the branch (`git push origin feature/your-feature-name`).
5.  Open a Pull Request.

---

## License

This project is distributed under the MIT License. See `LICENSE` for more information.