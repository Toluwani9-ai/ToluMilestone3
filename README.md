Travel Journal – Milestone 3

Local Storage, Room Database, MVVM Architecture, Jetpack Compose UI

This milestone builds on the previous work by adding persistent local storage using the Room Database. 
The app now allows users to create, store, and view travel journal entries (Trips) directly on the device.

Overview of Milestone 3

The goal of this milestone was to integrate a local database system into the Travel Journal application. My implementation uses:
-	Room Database for local offline storage.
-	DAO (Data Access Object) to handle database queries.
-	Repository layer to separate data logic
-	ViewModel + Factory for UI-friendly data handling
-	Jetpack Compose for all screens
-	MVVM architecture for clean structure and separation of concerns


The app now supports adding and displaying saved travel trips.

Features Implemented

-	 Room Database Integration: Created a Trip entity storing Title, Destination, Configured AppDatabase with Room to store data locally. and added TripDao with insert and query functions.

2. Repository Pattern
	•	Implemented TripRepository for clean data management.
	•	Keeps UI separate from database operations.
	•	Prevents direct DB access inside the UI.

⸻

3. MVVM Architecture
	•	TripViewModel exposes live data for the UI.
	•	TripViewModelFactory provides dependencies correctly.
	•	Ensures configuration-change safety (e.g., rotation).

⸻

4. Jetpack Compose Screens
	•	TripListScreen
Displays all saved trips in a clean, scrollable UI.
	•	AddTripScreen
Users can enter:
	•	Trip name
	•	Destination
	•	Date
	•	Notes
Then save the trip into the database.
	•	MainActivity
Loads the entire Compose app and attaches the TripViewModel.


