# ALX Travel App 0x00

## Milestone 2: Creating Models, Serializers, and Seeders

### Objective

This milestone focuses on setting up the database layer, serialization logic for API responses, and creating a database seeder for the travel listings application.

---

### Repository

- GitHub: [alx_travel_app_0x00](https://github.com/BunnyeNyash/alx_travel_app_0x00.git)
- Main Directory: `alx_travel_app`

### Project Structure
```
alx_travel_app/
├── listings/
│ ├── models.py
│ ├── serializers.py
│ └── management/
│ └── commands/
│ └── seed.py
├── manage.py
└── README.md
```

### Tasks Completed

#### 1. **Project Duplication**
- The original repository `alx_travel_app` was successfully duplicated into this new repository: `alx_travel_app_0x00`.

#### 2. **Models Implementation**
- Defined the following models in `listings/models.py`:
  - `Listing`: Represents a travel listing.
  - `Booking`: Represents a user's booking for a listing.
  - `Review`: Represents a review given by a user for a listing.
- Included appropriate fields, data types, relationships (`ForeignKey`, `OneToMany`, etc.), and constraints.

#### 3. **Serializers**
- Created `ListingSerializer` and `BookingSerializer` in `listings/serializers.py`.
- These serializers handle conversion between Django model instances and JSON format for API responses.

#### 4. **Seeder Command**
- Added a custom Django management command in `listings/management/commands/seed.py`.
- The command populates the database with realistic sample data for Listings (and optionally Bookings/Reviews).

#### 5. **Testing the Seeder**
- Verified the seeder by running:
```bash
python manage.py seed
```

- Sample listings were added successfully to the database.


### How to Use
1. Clone the Repository

```bash
git clone https://github.com/BunnyeNyash/alx_travel_app_0x00.git
cd alx_travel_app_0x00
```

2. Run Migrations

```bash
python manage.py migrate
```

3. Seed the Database

```bash
python manage.py seed
```

