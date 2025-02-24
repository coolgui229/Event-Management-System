import React, { useState, useEffect, useRef } from 'react';
import { BrowserRouter as Router, Route, Routes, Link, useNavigate, useParams } from 'react-router-dom';

// Custom Hook for form handling
function useForm(initialValues) {
  const [values, setValues] = useState(initialValues);
  const [errors, setErrors] = useState({});

  const handleChange = (e) => {
    const { name, value } = e.target;
    setValues({
      ...values,
      [name]: value,
    });
    // Resetting errors when input changes
    setErrors({ ...errors, [name]: '' });
  };

  const validate = () => {
    let tempErrors = {};
    if (!values.name) tempErrors.name = 'Event name is required';
    if (!values.date) tempErrors.date = 'Event date is required';
    if (!values.description) tempErrors.description = 'Event description is required';
    setErrors(tempErrors);
    return Object.keys(tempErrors).length === 0;
  };

  return [values, handleChange, validate, errors];
}

// Custom Hook for event handling
function useEvents() {
  const [events, setEvents] = useState([]);

  useEffect(() => {
    const storedEvents = JSON.parse(localStorage.getItem('events')) || [];
    setEvents(storedEvents);
  }, []);

  const addEvent = (event) => {
    const updatedEvents = [...events, event];
    setEvents(updatedEvents);
    localStorage.setItem('events', JSON.stringify(updatedEvents));
  };

  const deleteEvent = (id) => {
    const updatedEvents = events.filter((event) => event.id !== id);
    setEvents(updatedEvents);
    localStorage.setItem('events', JSON.stringify(updatedEvents));
  };

  return [events, addEvent, deleteEvent];
}

// Main App Component
function App() {
  return (
    <Router>
      <header>
        <nav style={styles.nav}>
          <Link style={styles.link} to="/">Dashboard</Link>
          <Link style={styles.link} to="/create">Create Event</Link>
        </nav>
      </header>
      <main style={styles.main}>
        <Routes>
          <Route path="/" element={<Dashboard />} />
          <Route path="/create" element={<CreateEvent />} />
          <Route path="/event/:id" element={<Event />} />
        </Routes>
      </main>
      <footer style={styles.footer}>
        <p>&copy; 2024 Event Manager. All Rights Reserved.</p>
      </footer>
    </Router>
  );
}

// Dashboard Component
function Dashboard() {
  const [events, , deleteEvent] = useEvents();

  const handleDelete = (id) => {
    if (window.confirm('Are you sure you want to delete this event?')) {
      deleteEvent(id);
    }
  };

  return (
    <div style={styles.container}>
      <h1 style={styles.heading}>Event Dashboard</h1>
      <ul style={styles.eventList}>
        {events.map((event) => (
          <li key={event.id} style={styles.eventItem}>
            <Link to={`/event/${event.id}`} style={styles.eventLink}>{event.name}</Link>
            <button onClick={() => handleDelete(event.id)} style={styles.deleteButton}>Delete</button>
          </li>
        ))}
      </ul>
    </div>
  );
}

// Create Event Component
function CreateEvent() {
  const [events, addEvent] = useEvents();
  const navigate = useNavigate();

  const handleEventSubmit = (eventData) => {
    addEvent({ ...eventData, id: Date.now() });
    navigate('/');
  };

  return (
    <div style={styles.container}>
      <h1 style={styles.heading}>Create New Event</h1>
      <EventForm onSubmit={handleEventSubmit} />
    </div>
  );
}

// Event Form Component
function EventForm({ onSubmit }) {
  const [values, handleChange, validate, errors] = useForm({ name: '', date: '', description: '' });
  const nameRef = useRef(null);

  const handleSubmit = (e) => {
    e.preventDefault();
    if (validate()) {
      onSubmit(values);
    }
  };

  return (
    <form onSubmit={handleSubmit} style={styles.form}>
      <input
        ref={nameRef}
        name="name"
        value={values.name}
        onChange={handleChange}
        placeholder="Event Name"
        style={styles.input}
      />
      {errors.name && <p style={styles.error}>{errors.name}</p>}
      <input
        name="date"
        value={values.date}
        onChange={handleChange}
        type="date"
        style={styles.input}
      />
      {errors.date && <p style={styles.error}>{errors.date}</p>}
      <textarea
        name="description"
        value={values.description}
        onChange={handleChange}
        placeholder="Event Description"
        style={styles.textarea}
      />
      {errors.description && <p style={styles.error}>{errors.description}</p>}
      <button type="submit" style={styles.button}>Create Event</button>
    </form>
  );
}

// Event Details Component
function Event() {
  const { id } = useParams();
  const [event, setEvent] = useState(null);

  useEffect(() => {
    const storedEvents = JSON.parse(localStorage.getItem('events')) || [];
    const foundEvent = storedEvents.find((event) => event.id === parseInt(id));
    setEvent(foundEvent);
  }, [id]);

  if (!event) {
    return <p style={styles.notFound}>Event not found.</p>;
  }

  return (
    <div style={styles.container}>
      <h1 style={styles.heading}>{event.name}</h1>
      <p>{event.date}</p>
      <p>{event.description}</p>
    </div>
  );
}

// Inline Styling for the Application
const styles = {
  nav: {
    display: 'flex',
    justifyContent: 'space-around',
    padding: '20px',
    backgroundColor: '#4A90E2',
    boxShadow: '0 4px 6px rgba(0, 0, 0, 0.1)',
  },
  link: {
    color: '#fff',
    fontSize: '18px',
    textDecoration: 'none',
    padding: '8px 16px',
    transition: 'background-color 0.3s, transform 0.3s',
  },
  main: {
    padding: '20px',
  },
  footer: {
    textAlign: 'center',
    padding: '20px',
    backgroundColor: '#f1f1f1',
    position: 'absolute',
    width: '100%',
    bottom: '0',
  },
  container: {
    maxWidth: '600px',
    margin: '0 auto',
    padding: '20px',
    textAlign: 'center',
  },
  heading: {
    color: '#4A90E2',
    marginBottom: '20px',
  },
  eventList: {
    listStyleType: 'none',
    padding: 0,
  },
  eventItem: {
    backgroundColor: '#fff',
    padding: '20px',
    marginBottom: '10px',
    boxShadow: '0 4px 8px rgba(0, 0, 0, 0.1)',
    borderRadius: '5px',
    transition: 'transform 0.3s',
  },
  eventLink: {
    textDecoration: 'none',
    color: '#4A90E2',
    fontSize: '18px',
  },
  deleteButton: {
    marginLeft: '15px',
    backgroundColor: '#FF4D4D',
    color: 'white',
    border: 'none',
    borderRadius: '5px',
    padding: '5px 10px',
    cursor: 'pointer',
    transition: 'background-color 0.3s',
  },
  deleteButtonHover: {
    backgroundColor: '#D63939',
  },
  form: {
    display: 'flex',
    flexDirection: 'column',
    width: '100%',
    maxWidth: '400px',
    margin: '0 auto',
    padding: '20px',
    backgroundColor: 'white',
    borderRadius: '10px',
    boxShadow: '0 4px 10px rgba(0, 0, 0, 0.1)',
  },
  input: {
    marginBottom: '15px',
    padding: '12px',
    border: '1px solid #ddd',
    borderRadius: '5px',
    fontSize: '16px',
  },
  textarea: {
    marginBottom: '15px',
    padding: '12px',
    border: '1px solid #ddd',
    borderRadius: '5px',
    fontSize: '16px',
  },
  button: {
    padding: '12px',
    backgroundColor: '#4A90E2',
    color: 'white',
    border: 'none',
    fontSize: '16px',
    borderRadius: '5px',
    cursor: 'pointer',
    transition: 'background-color 0.3s',
  },
  buttonHover: {
    backgroundColor: '#357ABD',
  },
  notFound: {
    textAlign: 'center',
    color: 'red',
  },
  error: {
    color: 'red',
    fontSize: '14px',
  },
};

export default App;
