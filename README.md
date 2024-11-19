# Jira Clone
ZCrum is a project management application inspired by Jira. It offers a comprehensive workflow for managing projects, Sprints, issues, and teams in an intuitive and user-friendly interface.

## Features

-   **Project Showcase & Carousel**: Highlighted features and testimonials from companies using ZCrum.
-   **User Onboarding**: Sign up/login with Google and email, organization creation, and role-based access control using Clerk.
-   **Protected Routes**: Ensures unauthorized users cannot navigate to restricted pages during onboarding.
-   **Organization Management**: Create, update, or delete organizations; invite and manage members.
-   **Project & Sprint Management**: Create multiple projects within organizations and plan Sprints.
-   **Issue Tracking**: Create, update, and manage issues with drag-and-drop support; priority, role-based actions, and search/filter functionalities.
-   **Form Management**: Uses React Hook Form and Zod for validation and schema management.
## Tech Stack

-   Next.js
-   React
-   Javascript
-   Prisma
-   Neondb
-   TailwindCSS
-   ShadCN

## Screenshots

![zcrum homepage](/public/jira-clone-homepage.png)
![organization page](/public/organization-dashboard.png)
![sprint page](/public/project-sprint-kanbanboard.png)

## Prerequisites

Before you begin, ensure you have the following installed on your local machine:

- **git** 
- **Node.js** (v16 or later) 
- **npm** (Node Package Manager)

## Local Setup

1. Clone the Repository

	```bash
	git clone https://github.com/kundusubrata/jira-clone.git
	cd jira-clone
	```
2. Install Dependencies
	```bash
	npm install
	```
3.  Configure Environment Variables
	Create a new file named `.env` in the root of your project and add the following content:
	```bash
	DATABASE_URL=
	NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
	CLERK_SECRET_KEY=
	NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
	NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
	NEXT_PUBLIC_CLERK_SIGN_IN_FALLBACK_REDIRECT_URL=/onboarding
	NEXT_PUBLIC_CLERK_SIGN_UP_FALLBACK_REDIRECT_URL=/onboarding
	```
	Sign up and create a new project on the [Clerk website](https://clerk.com) to obtain your Clerk credentials, and replace the placeholder values accordingly. Set up your Neon database by visiting [Neon db console](https://console.neon.tech/) to retrieve the necessary credentials. Ensure all required environment variables are configured properly.
	
4.  Set Up Prisma
	Run the following commands to generate Prisma client and apply database migrations:
	```
	npx prisma migrate deploy / npx prisma db push
	npx prisma db pull
	npx prisma generate
	npx prisma studio
	```
5. Run the Development Server
	```bash
	npm run dev
	```
	This will start the development server at `http://localhost:3000`.
6. Access the Application
	Open your browser and navigate to `http://localhost:3000` to see the  application in action.

## Contributing

Feel free to fork this repository, create a branch, and submit pull requests for any improvements or fixes.

