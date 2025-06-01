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
alx_travel_app_0x00/
├── alx_travel_app/
│   ├── listings/
│   │   ├── __init__.py
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── management/
│   │   │   └── commands/
│   │   │       └── seed.py
│   │   ├── migrations/
│   │   │   └── __init__.py
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── tests.py
│   │   ├── urls.py
│   │   └── views.py
│   ├── alx_travel_app/
│   │   ├── __init__.py
│   │   ├── asgi.py
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── wsgi.py
│   ├── db.sqlite3
│   ├── manage.py
│   └── requirements.txt
├── README.md
```

### Key Files and Their Roles
- listings/models.py: Defines the database models:

  - Listing: Represents a travel listing.
  - Booking: Represents a user's booking for a listing.
  - Review: Represents a user's review of a listing.

- listings/serializers.py: Contains serializers for the Listing and Booking models, facilitating the conversion between model instances and JSON representations for API interactions.

- listings/management/commands/seed.py: Implements a custom Django management command to seed the database with sample data for testing and development purposes.

- listings/views.py: Contains view functions or classes to handle HTTP requests and return responses.

- listings/urls.py: Maps URLs to the corresponding views in the listings app.

- alx_travel_app/settings.py: Configures the Django project's settings, including installed apps, middleware, database configurations, and more.

- manage.py: A command-line utility that lets you interact with this Django project in various ways.

- requirements.txt: Lists the Python packages required to run the project.

- README.md: Provides an overview of the project, setup instructions, and other relevant information.


### Functionality and Purpose
This Django project is designed to manage travel listings, bookings, and reviews. The primary functionalities include:

- Modeling: Defining the structure of the data with appropriate relationships and constraints.
- Serialization: Preparing data for API consumption by converting complex data types to native Python datatypes.
- Seeding: Populating the database with initial data to facilitate development and testing.



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

2. Create and activate a virtual environment:

```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Run Migrations

```bash
python manage.py migrate
```

5. Seed the Database

```bash
python manage.py seed
```

6. Run the development server:

```bash
python manage.py runserver
```

7. Access the application:

Open your browser and navigate to http://127.0.0.1:8000/ to view the application.
