

# Zapier

## Description

This project is a full-stack application designed with a microservices approach, consisting of a frontend, backend, processor, and worker components. It integrates with Solana blockchain, manages user authentication, and performs asynchronous tasks using workers.

## Features

- User authentication with email verification and password reset.
- Integration with Solana blockchain for transactions.
- Frontend built using Next.js and React, styled with TailwindCSS.
- Backend services built using Node.js, TypeScript, and Prisma for database management.
- Asynchronous task handling for email sending and blockchain reconciliation.

## Tech Stack

- **Frontend:**
  - Next.js
  - React.js
  - TailwindCSS
  - TypeScript

- **Backend & Processor:**
  - Node.js
  - TypeScript
  - Prisma
  - Solana Integration

- **Worker:**
  - Node.js
  - TypeScript
  - Kafka.js for messaging and async processing

## Installation Instructions

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd Zapier
   ```

2. Install dependencies for each service:

   - Frontend:
     ```bash
     cd frontend
     npm install
     ```

   - Backend:
     ```bash
     cd primary-backend
     npm install
     ```

   - Processor:
     ```bash
     cd processor
     npm install
     ```

   - Worker:
     ```bash
     cd worker
     npm install
     ```

3. Set up the database:
   Configure Prisma with your database credentials in `.env` files for each service that uses it (backend, processor, worker).

4. Run migrations:

   ```bash
   npx prisma migrate dev
   ```

5. Start each service:

   - Frontend:
     ```bash
     npm run dev
     ```

   - Backend, Processor, Worker:
     ```bash
     npm start
     ```

## Folder Structure

```
├── frontend
│   ├── app
│   ├── components
│   └── public
├── primary-backend
│   ├── prisma
│   └── src
├── processor
│   ├── prisma
│   └── src
├── worker
│   ├── prisma
│   └── src
```

## Future Enhancements

- Implement email verification before allowing user login.
- Add password reset functionality via email.
- Improve UI using `react-flow` for better user interaction.
- Solana reconciliation side quest: Ensure that transactions on the Solana blockchain are not processed twice when the worker recovers from downtime.
