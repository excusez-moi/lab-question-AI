# AI-Powered Lab Question Generation System

## 1. The Problem

In academic settings, particularly in lab-based courses, a recurring issue arises when all students receive the same question. This often leads to reduced learning efficiency, increased chances of plagiarism, and difficulty in conducting fair, unbiased evaluations. Traditional methods of creating varied questions are time-consuming and often result in inconsistent difficulty levels.

## 2. The Solution

This project is a robust, AI-powered system designed to automatically generate unique but equivalent lab questions for each student. The system leverages the power of OpenAI's GPT-4 to ensure that no two students receive the exact same question, while maintaining a consistent level of difficulty and fairness.

The application serves as an administrative dashboard for instructors to manage question templates, generate batches of questions, track student assignments, and monitor activity, ensuring a streamlined and equitable evaluation process.

## 3. Key Features

- **🤖 AI-Powered Question Generation**: Utilizes OpenAI GPT-4 to create unique and varied lab questions from a base template.
- **📝 Template-Based Approach**: Instructors can create question templates with variables that the AI uses to generate diverse problem sets.
- **⚖️ Consistent Difficulty**: AI is used to evaluate and maintain a consistent difficulty level across all generated questions, ensuring fairness.
- **👨‍🏫 Instructor Dashboard**: A comprehensive interface for instructors to manage students, question templates, assignments, and question batches.
- **🔐 Role-Based Access Control**: Secure authentication for instructors/admins using Replit's OpenID Connect.
- **📊 Tracking & Logging**: System for tracking assignments and logging all major activities for a complete audit trail.

## 4. System Architecture

This is a full-stack application built with a modern technology stack, focusing on performance, type safety, and a clean user experience.

### Frontend
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite
- **Routing**: Wouter for lightweight routing
- **State Management**: TanStack Query for server state caching and synchronization
- **Styling**: Tailwind CSS with shadcn/ui for the component library
- **Forms**: React Hook Form with Zod for robust validation

### Backend
- **Framework**: Express.js with TypeScript
- **API**: RESTful API design
- **Authentication**: Session-based authentication using Replit Auth (OpenID Connect)
- **ORM**: Drizzle ORM for type-safe database interactions
- **Database**: PostgreSQL

## 5. Tech Stack

| Category      | Technology                                                                                                                              |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Frontend**  | `React 18`, `TypeScript`, `Vite`, `Wouter`, `TanStack Query`, `React Hook Form`                                                             |
| **Backend**   | `Express.js`, `Node.js`, `tsx`                                                                                                          |
| **Database**  | `PostgreSQL`, `Drizzle ORM`, `Neon` (recommended serverless provider)                                                                     |
| **AI**        | `OpenAI GPT-4`                                                                                                                          |
| **Styling**   | `Tailwind CSS`, `shadcn/ui`, `Radix UI`, `Lucide React`                                                                                     |
| **Auth**      | `Replit Auth (OpenID Connect)`, `passport`, `express-session`                                                                             |
| **Validation**| `Zod`                                                                                                                                   |
| **Tooling**   | `ESBuild`, `Drizzle Kit`, `ESM`                                                                                                           |

## 6. Getting Started

Follow these instructions to get a local copy of the project up and running for development and testing purposes.

### Prerequisites
- Node.js (v20.x or higher recommended)
- npm or another package manager
- Access to a PostgreSQL database
- An OpenAI API key

### Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name
    ```

2.  **Install dependencies:**
    ```sh
    npm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of the project and add the necessary environment variables. This will include your database connection string, OpenAI API key, and session secret.
    ```env
    DATABASE_URL="your_postgresql_connection_string"
    OPENAI_API_KEY="your_openai_api_key"
    SESSION_SECRET="your_super_secret_session_key"
    # Add other variables as needed from Replit Auth configuration
    ```

4.  **Push database schema:**
    Apply the Drizzle ORM schema to your database.
    ```sh
    npm run db:push
    ```

5.  **Run the development server:**
    This command starts both the frontend and backend servers with hot-reloading.
    ```sh
    npm run dev
    ```

## 7. Available Scripts

This project comes with several scripts to help with development:

-   `npm run dev`: Starts the Vite development server for the frontend and the Express server for the backend using `tsx` for hot-reloading.
-   `npm run build`: Builds the production-ready frontend and backend into the `dist` directory.
-   `npm run start`: Starts the production server from the built files in `dist`.
-   `npm run check`: Runs the TypeScript compiler to check for type errors.
-   `npm run db:push`: Pushes the current Drizzle ORM schema to your database.

## 8. License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
