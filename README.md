\# 🚗 Vehicle Rental System



A full-stack \*\*MERN-based Vehicle Rental System\*\* that allows users to register, browse available vehicles, book vehicles, make online payments through Razorpay, and manage their bookings through a dedicated My Bookings section.



\---



\# 🚀 Tech Stack



\* \*\*React.js\*\*

\* \*\*JavaScript\*\*

\* \*\*HTML5 / CSS3\*\*

\* \*\*Node.js\*\*

\* \*\*Express.js\*\*

\* \*\*MongoDB / Mongoose\*\*

\* \*\*Razorpay Payment Gateway\*\*

\* \*\*REST API Architecture\*\*

\* \*\*Git \& GitHub\*\*

\* \*\*Vercel / Render\*\*



\---



\# 📂 Project Structure



```text

Vehicle-Rental-System/

│

├── client/

│   ├── public/

│   └── src/

│       ├── pages/

│       │   ├── Home.js

│       │   ├── Login.js

│       │   ├── Register.js

│       │   ├── Vehicles.js

│       │   └── MyBookings.js

│       │

│       ├── components/

│       ├── App.js

│       └── index.js

│

├── server/

│   ├── config/

│   │   └── db.js

│   │

│   ├── controllers/

│   │   ├── authController.js

│   │   ├── bookingController.js

│   │   └── paymentController.js

│   │

│   ├── models/

│   │   ├── User.js

│   │   └── Booking.js

│   │

│   ├── routes/

│   │   ├── authRoutes.js

│   │   ├── bookingRoutes.js

│   │   └── paymentRoutes.js

│   │

│   ├── server.js

│   └── package.json

│

└── README.md

```



\---



\# 🔐 Authentication



The system provides user authentication through registration and login functionality.



\### Features



\* User Registration

\* User Login

\* User information stored in MongoDB

\* Logged-in user identification using stored user information

\* Protected booking workflow



\---



\# 👤 User APIs



| Method | Route                | Description         |

| ------ | -------------------- | ------------------- |

| POST   | `/api/auth/register` | Register a new user |

| POST   | `/api/auth/login`    | Login user          |



\---



\# 🚗 Vehicle Management



Users can browse the available rental vehicles from the Vehicles section.



\### Available Vehicles



\* \*\*BMW Luxury Car\*\* — ₹2000/day

\* \*\*Royal Enfield Bike\*\* — ₹500/day

\* \*\*Range Rover SUV\*\* — ₹3000/day



\### Vehicle Information



\* Vehicle Name

\* Rental Price

\* Vehicle Image

\* Availability Status

\* Fuel Type

\* Self Drive Option

\* Rating



\---



\# 📅 Booking APIs



The booking module handles vehicle booking, retrieving user bookings and cancellation.



| Method | Route                             | Description          |

| ------ | --------------------------------- | -------------------- |

| POST   | `/api/booking/create`             | Create a new booking |

| GET    | `/api/booking/mybookings/:userId` | Get user's bookings  |

| DELETE | `/api/booking/cancel/:id`         | Cancel a booking     |



\---



\# 💳 Payment / Razorpay APIs



Razorpay is integrated into the project for online payment processing.



| Method | Route                       | Description                   |

| ------ | --------------------------- | ----------------------------- |

| POST   | `/api/payment/create-order` | Create Razorpay payment order |



\### Payment Flow



```text

User selects vehicle

&#x20;       ↓

Booking date entered

&#x20;       ↓

Backend creates Razorpay Order

&#x20;       ↓

Razorpay Checkout

&#x20;       ↓

Payment Successful

&#x20;       ↓

Booking Created

&#x20;       ↓

Booking stored in MongoDB

```



> Razorpay has been configured in \*\*Test Mode\*\* for project demonstration.



\---



\# 📖 My Bookings



The \*\*My Bookings\*\* section allows users to view their rental bookings.



Each booking displays:



\* Vehicle name

\* Vehicle image

\* Rental price

\* Booking date

\* Booking status

\* Cancel Booking option



\---



\# ❌ Cancel Booking



Users can cancel an existing booking using the \*\*Cancel Booking\*\* button.



The frontend sends a DELETE request to the backend, and the corresponding booking is removed from the database.



\---



\# 🔒 Backend \& REST APIs



The backend is built using \*\*Node.js and Express.js\*\*.



It handles:



\* User authentication

\* Booking creation

\* Booking retrieval

\* Booking cancellation

\* Razorpay order creation

\* MongoDB database operations



The frontend communicates with the backend through REST APIs.



\---



\# 🗄️ Database



\*\*MongoDB\*\* is used as the primary database and \*\*Mongoose\*\* is used for database interaction.



\### User Data



```text

User

&#x20;├── Name

&#x20;├── Email

&#x20;└── Password

```



\### Booking Data



```text

Booking

&#x20;├── User ID

&#x20;├── Vehicle

&#x20;├── Price

&#x20;├── Booking Date

&#x20;├── Payment ID

&#x20;└── Payment Status

```



\---



\# ⚙️ Installation



Clone the repository:



```bash

git clone https://github.com/ojhasuraj65/vehicle-rental-system.git

```



Go to the project directory:



```bash

cd vehicle-rental-system

```



Install frontend dependencies:



```bash

cd client

npm install

```



Install backend dependencies:



```bash

cd ../server

npm install

```



\---



\# ▶️ Run Application



\### Start Backend



```bash

cd server

npm run dev

```



Backend runs on:



```text

http://localhost:5000

```



\### Start Frontend



Open another terminal:



```bash

cd client

npm start

```



Frontend runs on:



```text

http://localhost:3000

```



\---



\# 🌐 Environment Variables



Create a `.env` file inside the `server` folder:



```env

PORT=5000

MONGO\_URI=your\_mongodb\_connection\_string



RAZORPAY\_KEY\_ID=your\_razorpay\_test\_key

RAZORPAY\_KEY\_SECRET=your\_razorpay\_test\_secret

```



Do not upload `.env` to GitHub.



\---



\# 📦 Core Features



\* User Registration \& Login

\* Vehicle Listing

\* Vehicle Price \& Availability Information

\* Booking Date Selection

\* Online Payment Integration

\* Razorpay Test Mode

\* My Bookings

\* Cancel Booking

\* MongoDB Database

\* REST APIs

\* Responsive React UI

\* Cloud Deployment



\---



\# ☁️ Deployment



The project has been deployed using:



\### Frontend



\*\*Vercel\*\*



```text

https://vehicle-rental-system-knf7.vercel.app/

```



\### Backend



\*\*Render\*\*



```text

https://vehicle-rental-system-1-fca8.onrender.com

```



\---



\# 🛠️ Development \& Testing Tools



\* \*\*Visual Studio Code\*\* — Development

\* \*\*Postman\*\* — API testing

\* \*\*Git\*\* — Version control

\* \*\*GitHub\*\* — Source code management

\* \*\*MongoDB Atlas\*\* — Cloud database

\* \*\*Vercel\*\* — Frontend deployment

\* \*\*Render\*\* — Backend deployment



\---



\# 🔮 Future Enhancements



\* Admin Dashboard

\* Vehicle Add / Update / Delete functionality

\* Real-time vehicle availability

\* Advanced search and filtering

\* Pickup and drop-off location management

\* Email/SMS booking notifications

\* User reviews and ratings

\* GPS-based vehicle tracking

\* Production payment integration

\* Rental history and analytics



\---



\# 👨‍💻 Author



\*\*Suraj Ojha\*\*



MERN Stack Developer



\### GitHub



https://github.com/ojhasuraj65/vehicle-rental-system



\### Live Project



https://vehicle-rental-system-knf7.vercel.app/



\---



\# 📜 License



This project is created for educational and internship purposes.



