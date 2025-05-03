# 🛠️ JobDone

**JobDone** is a user-driven mobile marketplace where individuals can post tasks they need help with and receive offers from service providers (fixers). Built using **Flutter** and powered by **Firebase**, the app allows seamless interaction between requesters and fixers, from posting jobs to chatting and reviewing completed work.

---

## Video Demo

<a href="https://www.youtube.com/watch?v=Nq4hqJfJCu8&t=4s" target="_blank">
  <img src="https://github.com/user-attachments/assets/aef0a976-b4a5-47ab-b536-61248476d19a" 
       alt="Click to watch demo video" width="300" height="600"/>
</a>

---

## Features

### 👤 Authentication
- Email/Password signup and login
- Role-based access: Customers vs. Fixers
- Forgot password functionality

### 📋 Job Posting (for Customers)
- Add/edit/delete jobs
- Upload multiple images for each job
- Specify available dates and time ranges
- View and accept offers from fixers

### 🛠️ Offer Management (for Fixers)
- Browse unassigned jobs
- Submit offers with pricing and availability
- See offer statuses (pending, accepted, rejected)

### 🗺️ Location-Aware
- Fixers can browse nearby jobs using an interactive **Google Map**

### 💬 In-App Chat
- Real-time messaging between users
- Supports both text and image messages
- Read receipts and timestamps

### 📊 Fixer Dashboard
- View total earnings
- Earnings breakdown by category
- View and edit public profile

---

## Project Structure

```
main.dart                          # App entry point and Firebase initialization
firebase_options.dart              # Firebase config for iOS & Android

models/
├── job_entry_model.dart           # Schema for job posts
├── offer_model.dart               # Schema for offers

views/
├── add_job_view.dart              # Create/edit job posts
├── job_list_view.dart             # Customer job dashboard
├── fixer_job_list_view.dart       # Available jobs for fixers
├── fixer_map_view.dart            # Location-based job listings
├── offers_view.dart               # Offers management
├── fixer_profile_view.dart        # Fixer earnings dashboard
├── chat_list_page.dart            # Chat conversations
├── ChatPage.dart                  # In-app messaging interface

controllers/
├── job_entry_service.dart         # Job CRUD logic
├── offer_service.dart             # Offer CRUD logic
├── chat_service.dart              # Chat creation and messaging logic
├── storage_service.dart           # Image upload to Firebase Storage
```

---

## Dependencies

### 🔐 Authentication & Firebase
- `firebase_core` – Initialize Firebase
- `firebase_auth` – Email/password authentication
- `cloud_firestore` – Firestore database for jobs, offers, and chats
- `firebase_storage` – Store job-related images and fixer documents
- `firebase_ui_auth` – Pre-built Firebase authentication UI
- `google_sign_in` – Google Sign-In integration

### 🗺️ Maps & Location
- `google_maps_flutter` – Display jobs on interactive maps
- `geolocator` – Access device location

### 📷 Media & Files
- `image_picker` – Pick and upload images
- `cached_network_image` – Load and cache images from URLs
- `carousel_slider` – Show images in a carousel view
- `pdf` – Create and render PDF documents
- `open_file` – Open files from the app
- `path_provider` – Access device file directories

### 💬 Chat & Messaging
- `timeago` – Display human-readable timestamps (e.g., "3h ago")

### ⚙️ Utilities & State Management
- `provider` – State management
- `uuid` – Generate unique IDs

---

## Getting Started

1. **Clone the repo**
   ```bash
   git clone https://github.com/znahamama/JobDone-App-.git
   cd dear-diary-app
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```
   
3. **Run the app**
   ```bash
   flutter run
   ```
   
---

##  License

This project is open source and available under the [MIT License](LICENSE).
