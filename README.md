# 🎓 Academic Virtualization Platform

## Project Overview

**Academic Virtualization Platform** is a full-stack web application designed to streamline and virtualize academic collaboration in an educational institute. It provides an online environment for managing class schedules, assignments, announcements (circulars), and peer-to-peer communication among students and faculty. The goal is to centralize academic activities—such as assignment submissions, note sharing, and group discussions—into a single, easy-to-use platform. By offering dedicated portals for students and teachers, the platform fosters better connectivity and engagement in an academic community.

## Features

### Student Portal

- **Class Schedules & Circulars:** View upcoming class schedules and important circulars or announcements from faculty.  
- **Assignments:** Submit assignments through the portal and track deadlines for each submission.  
- **Real-Time Discussions:** Participate in real-time group chats for academic discussions with classmates.  
- **Personal Dashboard:** Access a personalized dashboard showing your academic activities, upcoming deadlines, and recent announcements.

### Faculty Portal

- **Content Uploads:** Upload assignments, lecture notes, and announcements for students to access.  
- **Class Management:** Manage class schedules and student lists.  
- **Track Submissions:** Monitor student assignment submissions and engagement.  
- **Broadcast Announcements:** Send circulars or notifications to all students or specific groups/classes.

### Collaboration Tools

- **Real-Time Chat:** Integrated real-time chat feature (via REST-style updates) for students and teachers to interact.  
- **Notes Sharing:** Peer-to-peer note sharing and saving for future reference.  
- **Social Learning Network:** Follow peers or faculty; get intelligent recommendations based on academic interest.

## Technology Stack

- **Frontend:** React.js, Chakra UI, Pug (optional templating)
- **Backend:** Node.js, Express.js
- **Database:** MongoDB, Mongoose
- **Authentication & Security:** JWT, bcrypt, Helmet, express-mongo-sanitize, xss-clean
- **Email Service:** Nodemailer (SMTP, e.g., Gmail)
- **Utilities:** Multer (file upload), Morgan (logging), dotenv (env config)

## Project Structure

```
Academic-Virtualisation-REACT/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── app.js
│   └── server.js
├── frontend/
│   ├── src/
│   │   ├── Pages/
│   │   ├── static/
│   │   ├── App.js
│   │   └── index.js
│   ├── public/
│   └── README.md
├── assets/
│   ├── html/
│   ├── css/
│   └── js/
├── config.env
├── package.json
├── .gitignore
└── README.md
```

## Installation Instructions

### Prerequisites

- Node.js v14+
- npm
- MongoDB (local or cloud)

### Setup

```bash
git clone https://github.com/jenish-1990/Academic-Virtualisation-REACT.git
cd Academic-Virtualisation-REACT
```

#### Backend Setup

```bash
cd backend
npm install
```

#### Frontend Setup

```bash
cd frontend
npm install
```

#### Configure Environment

Create a `config.env` file in the root directory:

```env
# MongoDB connection
DATABASE=mongodb+srv://<USERNAME>:<PASSWORD>@cluster.mongodb.net/db
DATABASE_PASSWORD=your_password

# Server settings
NODE_ENV=development
PORT=3500

# JWT Auth
JWT_SECRET=your_secret_key
JWT_EXPIRES_IN=90d
JWT_COOKIE_EXPIRES_IN=90

# Email
EMAIL_USERNAME=your_email@gmail.com
EMAIL_PASSWORD=your_email_password
```

### Run Servers

Start backend:

```bash
cd backend
npm run dev
```

Start frontend:

```bash
cd frontend
npm start
```

Visit: [http://localhost:3000](http://localhost:3000)

## Configuration

See `.env` setup above. Required values include MongoDB URI, JWT secret, cookie expiration, and optional email service credentials.

## Usage Guide

- **Register/Login** via `/register` and `/login`
- **Dashboard** shows personal updates
- **Notes**: Upload, browse, save, delete
- **Assignments**: Students submit, faculty track
- **Instant Chat**: Real-time discussions
- **Community**: Follow/unfollow users
- **Profile**: View/edit your info, change password, delete account

## API Reference

### Auth

- `POST /api/v1/users/signup`
- `POST /api/v1/users/login`
- `GET /api/v1/users/logout`

### User Routes

- `PATCH /api/v1/users/follow`
- `PATCH /api/v1/users/unfollow`
- `PATCH /api/v1/users/save`
- `PATCH /api/v1/users/unsave`
- `PATCH /api/v1/users/updateMyPassword`
- `GET /api/v1/users/me`
- `PATCH /api/v1/users/updateMe`
- `DELETE /api/v1/users/deleteMe`

### Notes

- `GET /api/v1/notes`
- `POST /api/v1/notes/uploadNote`
- `DELETE /api/v1/notes/deleteNote`

## Testing

### Backend

Manual testing via Postman. Automated tests not yet included.

### Frontend

```bash
cd frontend
npm test
```

## Deployment

### Frontend

```bash
cd frontend
npm run build
```

Deploy `build/` to Netlify/Vercel or serve statically via Express:

```js
app.use(express.static(path.join(__dirname, '../frontend/build')));
app.get('*', (req, res) => {
  res.sendFile(path.join(__dirname, '../frontend/build/index.html'));
});
```

### Backend

```bash
cd backend
npm run start:prod
```

Use PM2 or deploy to Heroku, AWS, etc.

## Contribution Guidelines

1. Fork repo
2. Create feature branch
3. Commit descriptive messages
4. Run ESLint and format with Prettier
5. Submit pull request

### Linting

```bash
npm run lint
npm run format
```

## License

This project is licensed under the **Jenish Akhed**.

# Working Images

### Login & Registration
<img width="1512" height="949" alt="login" src="https://github.com/user-attachments/assets/63fb7d77-77ab-4d85-b5c8-bcc7f61fd496" />
<img width="1512" height="949" alt="regis" src="https://github.com/user-attachments/assets/795dda73-fd40-48bb-bcd7-711fdf7c273b" />

### Home
<img width="1512" height="949" alt="home" src="https://github.com/user-attachments/assets/9b60838d-fe21-4a2b-b65e-51931244811a" />

### My Profile
<img width="1512" height="982" alt="myprofile" src="https://github.com/user-attachments/assets/c9afac61-a4af-4532-932c-00314a62d4a8" />

### Edit Profile
<img width="1512" height="982" alt="edit" src="https://github.com/user-attachments/assets/120fe234-9a09-4a8b-a252-b927bb972f12" />

### My Uploads
<img width="1512" height="982" alt="myupload" src="https://github.com/user-attachments/assets/f307651d-1cec-4380-8608-befaff07801e" />

### Upload your own notes
<img width="1512" height="982" alt="upload" src="https://github.com/user-attachments/assets/43f893da-4a66-40f3-89a4-6f7cebc90094" />

### All Notes
<img width="1512" height="949" alt="notes" src="https://github.com/user-attachments/assets/bf6d6a1c-83f8-4b84-a066-a303d0ac43a1" />

### Notes Description
<img width="1512" height="949" alt="note_dec" src="https://github.com/user-attachments/assets/7e88d9ed-9eae-4c05-b342-9656584f5012" />

### Saved Notes
<img width="1512" height="982" alt="saved" src="https://github.com/user-attachments/assets/1947b54b-23bc-46f6-9747-736d190e9b89" />

### Community
<img width="1512" height="982" alt="community" src="https://github.com/user-attachments/assets/89f9fe13-f235-42ab-86c4-2ba149af6be7" />

### Community Info
<img width="1512" height="982" alt="community_dec" src="https://github.com/user-attachments/assets/e61ef946-83f5-4ca6-b9cc-61ddf2ae5a1f" />

### Contact US
<img width="1512" height="982" alt="contact" src="https://github.com/user-attachments/assets/344df06f-f782-4325-8796-a5ad0019d849" />
