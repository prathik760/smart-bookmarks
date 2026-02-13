# Smart Bookmark App

## Live Demo

https://smart-bookmarks-a5uc.vercel.app/

## GitHub Repository

https://github.com/prathik760/smart-bookmarks

---

## Overview

The Smart Bookmark App is a full-stack web application that allows users to securely save and manage personal bookmarks. Users authenticate using Google OAuth, and their bookmarks are stored privately. The application supports real-time updates, ensuring bookmarks added or deleted in one tab instantly reflect in other open sessions.

This project was built using Next.js (App Router), Supabase (Authentication, Database, Realtime), and Tailwind CSS, and deployed on Vercel.

---

## Features

* Google OAuth authentication (Supabase Auth)
* Add bookmarks (title and URL)
* Private bookmarks per user
* Real-time bookmark updates across tabs
* Delete bookmarks
* Secure Row Level Security (RLS)
* Fully deployed on Vercel

---

## Tech Stack

Frontend:

* Next.js (App Router)
* Tailwind CSS

Backend:

* Supabase

  * Authentication (Google OAuth)
  * PostgreSQL Database
  * Realtime subscriptions

Deployment:

* Vercel

---

## What I Learned

Before this project, I had heard about Supabase but had never used it in a real-world application. During this assignment, I researched and learned:

* How Supabase Auth works with Google OAuth
* How Supabase automatically manages users and sessions
* How to design database tables with proper structure
* How Row Level Security (RLS) ensures user data privacy
* How Supabase Realtime works using subscriptions
* How to integrate Supabase with Next.js App Router
* How authentication and session management works in production

This project helped me understand full-stack architecture using a Backend-as-a-Service platform.

---

## Challenges Faced and Solutions

### 1. Supabase Authentication Setup

**Challenge:**
Initially, configuring Google OAuth with Supabase and Google Cloud Console was confusing, especially redirect URIs and provider configuration.

**Solution:**
I researched Supabase documentation and Google OAuth flow to correctly configure Client ID, Client Secret, and redirect URLs.

---

### 2. Row Level Security (RLS) Policies

**Challenge:**
Without proper RLS policies, users could not access or insert data.

**Solution:**
I learned how to create SELECT, INSERT, and DELETE policies using `auth.uid()` to restrict access to only the logged-in user's bookmarks.

---

### 3. Realtime Updates

**Challenge:**
Understanding how realtime subscriptions work and ensuring UI updates automatically without refresh.

**Solution:**
I implemented Supabase realtime channels and subscribed to database changes using `postgres_changes`.

---

### 4. Authentication Persistence

**Challenge:**
Handling user session and protecting routes from unauthorized access.

**Solution:**
Used Supabase's built-in session handling and Next.js client components to manage authentication state.

---

### 5. Deployment Configuration

**Challenge:**
Google OAuth did not work initially after deployment due to incorrect redirect URLs.

**Solution:**
Updated Supabase Site URL and redirect URLs to match the Vercel deployment domain.

---

## Security

* Row Level Security ensures users can only access their own bookmarks
* Supabase handles authentication securely
* Environment variables protect sensitive keys

---

## How to Run Locally

```bash
git clone https://github.com/prathik760/smart-bookmarks.git

cd smart-bookmarks

npm install

npm run dev
```

---

## Future Improvements

* Edit bookmark feature
* Bookmark categories
* Bookmark search and filtering
* Better UI and UX
* Loading states and error handling

---

## Conclusion

This project helped me gain hands-on experience building a full-stack application using modern tools like Next.js and Supabase. It improved my understanding of authentication, database security, realtime systems, and deployment workflows.

---
