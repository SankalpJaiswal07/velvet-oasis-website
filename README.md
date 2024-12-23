# Velvet Oasis Website

## Live Demo

[View Live Demo](https://velvet-oasis-website.vercel.app/)

## Project Requirements from the Business

### User Types
- **Potential Guests**: Users who are exploring the hotel and its offerings but have not yet made a reservation.
- **Actual Guests**: Users who have made a reservation and are planning to or have stayed at the hotel.

### Functional Requirements

1. **Information Accessibility**
   - Guests should be able to learn all about Velvet Oasis Hotel, including its amenities, location, and services.

2. **Cabin Information**
   - Guests should be able to view detailed information about each cabin, including descriptions, images, and amenities.
   - Guests should be able to see the availability of each cabin by viewing booked dates on a calendar.

3. **Filtering Cabins**
   - Guests should be able to filter cabins based on their maximum guest capacity to find the most suitable option.

4. **Reservation System**
   - Guests should be able to reserve a cabin for a specific date range.
   - Reservations are not paid online. Payments will be made at the property upon arrival. Therefore, new reservations should be set to "unconfirmed" (booked but not yet checked in).

5. **Reservation Management**
   - Guests should be able to view all their past and future reservations in a user-friendly manner.
   - Guests should be able to update or delete a reservation if needed.

6. **User Authentication**
   - Guests need to sign up and log in before they can reserve a cabin and perform any operation.
   - Upon signing up, each guest should get a profile in the database.

7. **Profile Management**
   - Guests should be able to set and update basic data about their profile to make the check-in process at the hotel faster.

## Technology Decisions

- **Framework**
  - **NEXT.JS**: Chosen for its robust features and performance benefits, including server-side rendering and static site generation.

- **UI State Management**
  - **Context API**: Used for managing global state across the application to ensure a seamless user experience.

- **Database/API**
  - **Supabase**: Utilized for its real-time capabilities and ease of integration for managing the backend database and APIs.

- **Styling**
  - **Tailwind CSS**: Selected for its utility-first approach, enabling rapid and responsive UI development.

- **Deployment**
  - **Vercel**: Preferred for its seamless integration with Next.js, providing a straightforward deployment process and excellent performance.

## Setup Instructions

### Prerequisites
1. Node.js (v14 or higher)
2. npm or yarn package manager
3. Supabase account
4. Vercel account

### Steps to Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/velvet-oasis.git
   cd velvet-oasis
   ```

2. **Install Dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Environment Variables**
   - Create a `.env.local` file in the root directory.
   - Add the following environment variables:
     ```env
     NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
     NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
     ```

4. **Configure Supabase**
   - Sign in to your Supabase account.
   - Create a new project.
   - Copy the `API URL` and `anon key` from the Supabase dashboard to your `.env.local` file.
   - Create the necessary tables for users, cabins, and reservations in the Supabase database.

5. **Run the Development Server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```
   - Open [http://localhost:3000](http://localhost:3000) to see your application in the browser.

6. **Deploy to Vercel**
   - Sign in to your Vercel account.
   - Import your repository to Vercel.
   - Set up the environment variables in the Vercel project settings, using the same keys from your `.env.local` file.
   - Deploy the project.
