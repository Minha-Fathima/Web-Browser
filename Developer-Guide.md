# 🛠️ Developer Guide for Custom Web Browser

This guide explains the organization, design, and technologies behind the web browser application, providing details to help developers understand and extend its functionality.

---

## 🏗️ Class Organization and Responsibilities

### **UI Layer**
- **BrowserForm**: Handles core browser operations.
  - `Browse_Click`: Sends an HTTP request and displays the response.
  - `NavigateToUrl`: Navigates to a specified URL and updates the history.
  - `Reload_Click`: Reloads the current page.
  - `SetHomePage_Click`: Sets the homepage URL.
  - `BulkDownload_Click`: Initiates bulk download operations from a text file.
  - Manages navigation stacks with `_backStack` and `_forwardStack`.
  - Implements keyboard shortcuts in `BrowserForm_KeyDown` for user actions (e.g., navigating back, forward, refreshing, or managing history and favourites).

- **FavouritesForm**: Manages favourites.
  - `FavAdd_Click`: Adds a new favourite to the list.
  - `FavEdit_Click`: Edits an existing favourite.
  - `FavDelete_Click`: Deletes a selected favourite.
  - `FavList_Click`: Triggers navigation to the selected favourite URL via the `NavigateToUrlDelegate` delegate.
  - `ReloadFavourites()`: Reloads the displayed list of favourites after modifications to show real-time changes.

---

### **Managers Layer**
- **ManageHistory**: Manages browser history, ensuring persistence across sessions.
  - `LoadHistory`: Loads browsing history from the database on startup.
  - `SaveHistory`: Saves a new URL to the history list.
  - Connects directly to the database for persistence via `IManageDatabase`.

- **ManageFavourites**: Handles favourites management.
  - `LoadFavourites`: Loads all favourite entries.
  - `AddFavourite`, `UpdateFavourite`, `RemoveFavourite`: Methods to modify favourites data in the database.
  - Ensures consistency in the user's favourites list in collaboration with `FavouritesForm`.

- **ManageHomePage**: Manages the homepage URL using JSON storage.
  - `LoadHomePage`: Loads the homepage URL from `Settings.json`.
  - `SaveHomePageUrl`: Saves a new homepage URL to `Settings.json`.
  - Allows users to persistently set a custom homepage.

- **ManageDownload**: Handles bulk downloads.
  - `StartBulkDownload`: Initiates downloads from a specified file, with results displayed in `BrowserForm`.
  - Uses a delegate (`ResultHandler`) to process asynchronous bulk download completion.

---

### **Network Layer**
- **HttpService**: Handles HTTP requests and responses.
  - `FetchUrlContentAsync`: Asynchronously fetches content from a URL and returns an `HttpResponse` object containing:
    - Status code
    - Reason phrase
    - HTML content
  - Utilizes `HttpClient` for network operations with exception handling for HTTP errors, timeouts, and task cancellations.

---

### **Database Layer**
- **ManageDatabase**: Manages SQLite database setup and access for history and favourites.
  - `InitializeDatabase`: Sets up the database if it does not exist.
  - `LoadHistory`, `AddHistory`: Methods to load and save history records.
  - `LoadFavourites`, `AddFavourite`, `UpdateFavourite`, `RemoveFavourite`: Methods for interacting with favourites.
  - Abstracts database operations to ensure consistency for `ManageHistory` and `ManageFavourites`.

---

### **Models Layer**
- **HttpResponse**: Represents HTTP response data, including:
  - `StatusCode`
  - `ReasonPhrase`
  - `Content`
- **FavouritePage**: Defines the structure of a favourite item (e.g., Name, URL).
- **HomePageSettings**: Represents the homepage data structure for JSON serialization.

---

## 🛠️ Core Technologies and Libraries

- **HTTP Communication**:
  - `HttpClient` (in `HttpService`) is used for asynchronous network requests to retrieve and display webpage HTML and HTTP status codes.

- **Persistent Data Management**:
  - **SQLite**: Stores history and favourites, managed by `ManageDatabase`.
  - **JSON**: Stores homepage settings in a lightweight file (`Settings.json`), managed by `ManageHomePage`.

- **GUI Framework**:
  - Windows Forms, using buttons, list boxes, and event-driven methods to support user interactions.

- **Standalone Executable File**:
  - Created using **Inno Setup**, a Windows installation system for generating the standalone executable file.

---

## ⚙️ Extension Ideas
- Add more robust error handling for advanced HTTP responses and network security.
- Enhance GUI with modern frameworks like WPF or third-party libraries.
- Introduce additional customization options for themes or layouts.
- Implement automated testing for the entire application.

For further details or questions, contact the project maintainer at avoorminha@gmail.com.
