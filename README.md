# Next.js Starter Project

## Project Overview
This is a Next.js application demonstrating advanced routing patterns, particularly the use of route groups for authentication flows. The project showcases:

1. Route groups (via the `(auth)` folder) that:
   - Keep auth-related routes organized
   - Share common layout components
   - Maintain clean URL paths (/login, /signup)

2. A basic implementation with:
   - Authentication pages (login/signup)
   - Regular content pages (blogs, user)
   - TypeScript and Tailwind CSS integration

## Technology Stack
- **Framework**: Next.js 15.3.4
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **HTTP Client**: Axios
- **State Management**: (Add if applicable)
- **Testing**: (Add if applicable)

## Getting Started

### Prerequisites
- Node.js (v16 or later recommended)
- npm or yarn

### Installation
1. Clone the repository
2. Install dependencies:
```bash
npm install
# or
yarn install
```
3. Create `.env.local` file if needed

### Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser

## Route Groups Feature

This project demonstrates Next.js route groups through the `(auth)` folder. Route groups allow you to:

1. Organize routes without affecting the URL structure
2. Share layouts between routes
3. Create logical groupings of routes

### Example Route Groups

- `(auth)` group:
  - `/signup` - User registration
  - `/login` - User authentication
  - Shared layout with header/footer

Route groups are created by wrapping folder names in parentheses: `(groupname)`

### Key Benefits
- Maintain clean URL paths while organizing files
- Apply shared layouts to grouped routes
- Opt routes into specific layouts or behaviors

## Project Structure
```
my-app/
├── app/
│   ├── (auth)/           # Auth route group
│   │   ├── login/       # /login route
│   │   ├── signup/      # /signup route
│   │   └── layout.tsx   # Shared auth layout
│   ├── blogs/           # Regular route
│   └── user/            # Regular route
├── public/         # Static files
├── src/
│   ├── components/ # Reusable components
│   ├── styles/     # Global styles
│   ├── types/      # TypeScript types
│   └── utils/      # Utility functions
├── .env.local      # Environment variables
├── next.config.ts  # Next.js configuration
└── tailwind.config.js # Tailwind configuration