
# Event Management System

## Overview
This is a comprehensive Event Management System built using JavaScript, CSS, and MySQL. It allows users to create, manage, and register for events seamlessly. The system supports user authentication, event scheduling, ticketing, and real-time updates.

## Features
- **User Authentication**: Sign up and login functionality for event organizers and participants.
- **Event Creation**: Organizers can create and manage events, add details such as date, location, and description.
- **Event Registration**: Users can browse events and register for them.
- **Event Scheduling**: Organizers can set event dates, times, and venues.
- **Ticketing**: Automatic ticket generation upon registration.
- **Real-time Updates**: Notifications for event changes or updates.

## Technologies Used
- **Frontend**: JavaScript, CSS
- **Backend**: Node.js (JavaScript)
- **Database**: MySQL
- **Other**: Express.js for routing

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/event-management-system.git
   ```

2. Install dependencies:
   ```bash
   cd event-management-system
   npm install
   ```

3. Set up MySQL database and configure connection settings in `config/database.js`.

4. Start the server:
   ```bash
   npm start
   ```

5. Access the system in your browser at `http://localhost:3000`.

## Usage

1. Sign up or log in as an organizer or a participant.
2. As an organizer, create and manage events.
3. As a participant, browse events and register for them.
4. Organizers can view registered participants and send notifications.

## Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.
