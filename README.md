# voiceTOtext

The zip file contains the following files:

1. **index.html**
2. **save_text.php**

Let's start by looking at the contents of each file to understand them in detail. I'll display their contents next.

### Contents of `index.html`

This HTML file provides a simple web interface for voice-to-text conversion. Here's a breakdown of its structure and functionality:

1. **HTML Structure**:
    - The document has a basic HTML structure with a `head` and `body` section.
    - Includes a link to Google Fonts to use the "Poppins" font.

2. **CSS Styling**:
    - Styles are defined for the body, container, headings, buttons, and the output area to make the page visually appealing.

3. **JavaScript Functionality**:
    - The script starts by checking if the browser supports the Web Speech API.
    - Functions to handle speech recognition for Arabic (`ar-AR`) and English (`en-US`).
    - Listens for the result of the speech recognition and displays the final transcript.
    - Sends the recognized text to a server-side script (`save_text.php`) using an XMLHttpRequest.

4. **Buttons and Event Listeners**:
    - Two buttons: one for recognizing Arabic speech and another for English.
    - Event listeners are attached to these buttons to initiate speech recognition in the respective languages.

### Contents of `save_text.php`

This PHP file handles the server-side processing to save the recognized text into a MySQL database. Here's a detailed explanation:

1. **Error Reporting**:
    - PHP settings are configured to display all errors for debugging purposes.

2. **Database Connection**:
    - Connection details for the MySQL database are specified (host, user, password, database name).
    - A connection is established using `mysqli`.

3. **Handling the POST Request**:
    - The script checks if the `text` parameter is set in the POST request.
    - Prepares an SQL statement to insert the received text into the `text_table` in the database.
    - Binds the text parameter to the SQL statement and executes it.

4. **Exception Handling**:
    - Various checks and exception handling to catch and display errors during the database connection, statement preparation, and execution.

5. **Response**:
    - Sends a success message if the text is saved successfully, otherwise displays the error message.

### Summary

- **index.html** provides a user interface for capturing speech and converting it to text.
- **save_text.php** handles the backend operation of saving the captured text into a database.

These two files together form a basic voice-to-text application with support for both Arabic and English languages.

# Result 

https://github.com/user-attachments/assets/2dcbda99-84c9-4e51-871a-9e4b8709ac7d

