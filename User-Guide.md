# 📖 User Guide for Custom Web Browser

## 1. Installation
Navigate to the Standalone Executable Folder and run `WebBrowser-Final.exe` installer to install the application in your desired file location.

---

## 2. Launching the Application
- After installation, the application will launch by default. 
- If it doesn’t launch automatically, navigate to the installation folder and run the `WebBrowser` application file.
- The application opens with the homepage loaded.
  - By default, the homepage is set to the university’s website, but it can be customized.

![image](https://github.com/user-attachments/assets/6bf0b60b-4888-4a95-8293-4db2cab705d8)

---

## 3. Browsing a Web Page
- Enter a URL in the address bar and press **Enter** or click the **Browse** button.
- If the URL is invalid or does not begin with `http://` or `https://`, an error message will appear.
- Once loaded, the browser displays:
  - The raw HTML content in the main content area.
  - The HTTP status and page title in the window’s title bar.

![image](https://github.com/user-attachments/assets/ff8721c6-30ba-4a54-86f7-af24a0332025)


---

## 4. Navigation Controls
- Use the **Back** and **Forward** buttons to navigate through previously viewed pages.
- Use the **Home** button to navigate back to the homepage from any page.
- Use the **Reload** button to refresh the current page, fetching its content again from the server.

### Shortcuts:
- **Alt + Left Arrow**: Go back to the previous page.
- **Alt + Right Arrow**: Move forward to the next page.
- **Ctrl + R**: Reload the current page.

![image](https://github.com/user-attachments/assets/6f099dd3-88e0-49c1-830e-e9ee5a406157)

---

## 5. Setting and Accessing the Homepage
- To set the current page as the homepage, use the **Set Home Page** button or press **Ctrl + F5**.
- The homepage will load automatically each time the application starts.

![image](https://github.com/user-attachments/assets/dd8333be-9758-4c71-b176-da00e4c7249d)

---

## 6. Viewing and Managing Favourites
- Click on the **Favourites** button or press **Ctrl + D** to open the favourites form and save the current page to the favourites list.
  - The current page’s URL will automatically populate the input field.
  - Optionally, give the favourite a name or save the URL by clicking **Add**.
- View the favourites list in the favourites form:
  - Click once on a favourite to navigate to its page.
  - Double-click a favourite to edit it and save changes by clicking **Edit**.
  - Select a favourite and click **Delete** to remove it from the list.

![image](https://github.com/user-attachments/assets/a3d83aac-daad-4034-a8f5-5e882f1bf7c6)

---

## 7. Browsing History
- Access browsing history by clicking the **History** button in the main browser window or pressing **Ctrl + H**.
- The history list shows previously visited URLs with the most recent at the top.
- Click on a URL in the history list to navigate directly to the site.

![image](https://github.com/user-attachments/assets/2ba513d2-04e7-4166-9ce5-d051d964e758)

---

## 8. Bulk Download Web Pages
- Use the **Bulk Download** button or press **Ctrl + B** to select a text file (default: `bulk.txt`) containing URLs (one URL per line).
- The browser retrieves each URL and displays:
  - The response code.
  - The byte count.
  - The URL in the content area.

![image](https://github.com/user-attachments/assets/5e2d6267-0350-4f5f-8222-6b9f46a0b49b)

---

## 9. Error Handling and Messages
- The application provides clear error messages for:
  - Invalid or missing URLs.
  - HTTP request errors (e.g., `404 Not Found`, `403 Forbidden`).
- For unexpected errors, a descriptive error message will be displayed on the screen.

![image](https://github.com/user-attachments/assets/56e193b2-993c-48a4-b2dd-544c096dc6f7)

---

For additional support, please contact the project maintainer at avoorminha@gmail.com.
