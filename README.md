# 📖 Custom Web Browser

This is a custom web browser application developed as part of the **F20SC Industrial Programming** course. The application, built using **.NET C#** and **Windows Forms**, provides essential browsing functionalities, including navigation, history tracking, bookmark management, and bulk downloading. Designed with a layered architecture, it is scalable, user-friendly, and efficient for personal use on **Windows 11**.

Developed by:
- Minha Fathima Avoor

---

## 🚀 Features

### Core Functionalities:
- **Web Browsing**: Navigate to web pages by entering a URL.
- **History Management**: Automatically tracks and displays visited URLs.
- **Bookmarking**:
  - Save web pages as favorites.
  - Edit or delete bookmarks.
- **Navigation Controls**:
  - Navigate back and forward.
  - Reload pages.
  - Set and customize the homepage.
- **Bulk Download**:
  - Retrieve and display content from multiple URLs specified in a text file.

### User-Friendly Interface:
- Intuitive GUI built with **Windows Forms**.
- Shortcut keys for common actions:
  - **Ctrl + R**: Reload current page.
  - **Alt + Left Arrow**: Navigate back.
  - **Alt + Right Arrow**: Navigate forward.
  - **Ctrl + D**: Open Favorites form.
  - **Ctrl + H**: Open History list.
  - **Ctrl + B**: Bulk download.

### Advanced Features:
- **Error Handling**: Displays clear messages for invalid URLs and HTTP errors.
- **Persistence**: Saves history, bookmarks, and homepage settings across sessions.
- **Async/Await**: Ensures responsive UI during network operations.

---

## 🛠️ Technologies Used
- **Programming Language**: C#
- **Framework**: .NET with Windows Forms
- **Networking**: `HttpClient` for asynchronous HTTP requests.
- **Data Persistence**:
  - **SQLite** for history and bookmarks.
  - **JSON** for homepage settings.
- **Delegates**: Used for callback functions (e.g., bulk download results).

---

## 📂 Project Structure

### Layered Architecture:
1. **UI Layer**:
   - **BrowserForm**: Manages the main browser operations.
   - **FavouritesForm**: Handles bookmark management.
2. **Network Layer**:
   - **HttpService**: Manages HTTP requests and responses.
3. **Manager Layer**:
   - **ManageHistory**: Tracks and persists browsing history.
   - **ManageFavourites**: Handles bookmark operations.
   - **ManageHomePage**: Manages homepage settings.
   - **ManageDownload**: Manages bulk downloads.
4. **Database Layer**:
   - **ManageDatabase**: Interacts with SQLite for persistent data.
5. **Models Layer**:
   - Defines lightweight data structures (e.g., `FavouritePage`, `HttpResponse`).

---

## 🧑‍💻 Installation and Usage

The application offers a simple Browser GUI. For a detailed guide on application usage see [User Guide](User-Guide.md).
.

---

## 📫 Contact
For questions or feedback, please contact me: avoorminha@gmail.com .
