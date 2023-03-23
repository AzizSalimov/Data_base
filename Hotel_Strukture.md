# Hotel Structure

# Guests

```sql
CREATE TABLE guests (
  id SERIAL PRIMARY KEY,
  first_name VARCHAR(50) NOT NULL,
  last_name VARCHAR(50) NOT NULL,
  email VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  address VARCHAR(255) NOT NULL
);
```


# Rooms 

```sql
CREATE TABLE rooms (
  id SERIAL PRIMARY KEY,
  room_number VARCHAR(10) NOT NULL,
  floor INTEGER NOT NULL,
  capacity INTEGER NOT NULL,
  price NUMERIC(10,2) NOT NULL,
  is_booked BOOLEAN NOT NULL DEFAULT FALSE
);
```


# Room_type 


```sql
CREATE TABLE room_types (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  description TEXT NOT NULL
);

```


# Room_type_price

```sql
CREATE TABLE room_type_prices (
  id SERIAL PRIMARY KEY,
  room_type_id INTEGER REFERENCES room_types(id) ON DELETE CASCADE,
  start_date DATE NOT NULL,
  end_date DATE NOT NULL,
  price NUMERIC(10,2) NOT NULL
);
```

# Bookings

```sql
CREATE TABLE bookings (
  id SERIAL PRIMARY KEY,
  guest_id INTEGER REFERENCES guests(id) ON DELETE CASCADE,
  room_id INTEGER REFERENCES rooms(id) ON DELETE CASCADE,
  check_in_date DATE NOT NULL,
  check_out_date DATE NOT NULL,
  price NUMERIC(10,2) NOT NULL,
  is_paid BOOLEAN NOT NULL DEFAULT FALSE
);
```

# Payments

```sql
CREATE TABLE payments (
  id SERIAL PRIMARY KEY,
  booking_id INTEGER REFERENCES bookings(id) ON DELETE CASCADE,
  amount NUMERIC(10,2) NOT NULL,
  payment_date TIMESTAMP NOT NULL DEFAULT NOW()
);
```

# Discounts

```sql
CREATE TABLE discounts (
  id SERIAL PRIMARY KEY,
  code VARCHAR(20) NOT NULL,
  start_date DATE NOT NULL,
  end_date DATE NOT NULL,
  amount NUMERIC(10,2) NOT NULL,
  is_active BOOLEAN NOT NULL DEFAULT TRUE
);
```

# Room Type Discounts

```sql
CREATE TABLE room_type_discounts (
  id SERIAL PRIMARY KEY,
  room_type_id INTEGER REFERENCES room_types(id) ON DELETE CASCADE,
  discount_id INTEGER REFERENCES discounts(id) ON DELETE CASCADE
);

```

# Amenities

```sql
CREATE TABLE amenities (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  description TEXT NOT NULL
);
```

# Room Amenities

```sql
CREATE TABLE room_amenities (
  id SERIAL PRIMARY KEY,
  room_id INTEGER REFERENCES rooms(id) ON DELETE CASCADE,
  amenity_id INTEGER REFERENCES amenities(id) ON DELETE CASCADE
);
```

# Services

```sql
CREATE TABLE services (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  price NUMERIC(10,2) NOT NULL,
  description TEXT NOT NULL
);

```

# Service_bookings

```sql
CREATE TABLE service_bookings (
  id SERIAL PRIMARY KEY,
  booking_id INTEGER REFERENCES bookings(id) ON DELETE CASCADE,
  service_id INTEGER REFERENCES services(id) ON DELETE CASCADE,
  quantity INTEGER NOT NULL
);
```


# Users

```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  username VARCHAR(50) NOT NULL UNIQUE,
  password VARCHAR(255) NOT NULL,
  is_admin BOOLEAN NOT NULL DEFAULT FALSE
);
```

# User Sessions

```sql
CREATE TABLE user_sessions (
  id SERIAL PRIMARY KEY,
  user_id INTEGER REFERENCES users(id) ON DELETE CASCADE,
  token VARCHAR(255) NOT NULL UNIQUE,
  expiration TIMESTAMP NOT NULL
);
```

# All Tables

![image](https://user-images.githubusercontent.com/122611579/227101867-982e8aa6-617f-4864-a591-3391ba416e79.png)

