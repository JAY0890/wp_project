

## Project Name: Event Flux
## Category: Education and Learning Syetem

## Descriptio: Event flux let's student register for an event in collage campus like a seminar/guest lecture etc.. it has mainly two modules admin and user.every event has limited seats 



## User Roles

    Student: Can register/login, view all events, book seats, and view their personal dashboard.

    Admin: Can create new events (with image upload), modify event details, and view attendee rosters.


## if a student tries to book after all seats are full. we can deny them or add them in a queue. 


* **Module 1: Setup & Modern Practices**
    * Built with ES6+ syntax and `async/await`.
    * Uses `.env` for secure credential management (DB URIs, JWT Secrets).
    * Follows industry-standard MVC (Model-View-Controller) architecture.

* **Module 2: Backend & Routing**
    * REST API built on Express.js.
    * Modular routing (`/api/auth`, `/api/events`) separated from controller logic.

* **Module 3: Database Integration**
    * **MongoDB/Mongoose:** Strict schema validation for Users and Events.
    * **Atomic Booking Engine:** Uses `findOneAndUpdate` with conditional logic (`booked < capacity`) to ensure data integrity during concurrent requests.

* **Module 4: Authentication & Security**
    * **JWT (JSON Web Tokens):** Stateless authentication for session management.
    * **Bcrypt:** Password hashing to ensure no plain-text credentials are stored.
    * **RBAC:** Middleware restricts "Create Event" access to Admins only.

* **Module 5: File Upload**
    * **Multer Integration:** Handles image uploads for event posters.
    * Images are stored locally in an `/uploads` directory and referenced via file paths in the database.

* **Module 6: Error Handling**
    * Centralized error middleware standardizes responses (400, 401, 500) for validation failures and server errors.

