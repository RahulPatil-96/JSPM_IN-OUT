# Inward-Outward Portal

## Description
Inward-Outward Portal is an Electron-based Document Management System designed to manage inward and outward documents efficiently. It provides features such as user authentication, document CRUD operations, document approval, file previews, and automated backups.

## Features
- User login and authentication
- Insert, update, delete, and fetch documents with filters
- Document approval workflow
- Download search results in various formats
- File preview support for images, PDFs, and Word documents
- Automated daily backup of database and uploaded files
- Single instance application to prevent multiple app instances
- Built with Electron for cross-platform desktop support

## Installation

1. Ensure you have [Node.js](https://nodejs.org/) installed (version 16 or higher recommended).
2. Clone the repository or download the source code.
3. Navigate to the project directory:
   ```bash
   cd d:/project/jspm
   ```
4. Install dependencies:
   ```bash
   npm install
   ```

## Usage

To start the application in development mode, run:
```bash
npm start
```

This will launch the Electron app. The main window will open with the login screen.

## Build

To build the application for distribution, run:
```bash
npm run build
```

The build output will be located in the `dist` directory. The build configuration uses `electron-builder` with NSIS installer for Windows.

## Project Structure

- `main.js`: Main Electron process script, handles app lifecycle, IPC, and backup scheduling.
- `backend.js`: Database management and business logic (not detailed here).
- `preload.js`: Preload script for context isolation and secure IPC.
- `render.js`: Renderer process script (UI logic).
- `templates/`: HTML templates for different app views (login, dashboard, edit, search, etc.).
- `assets/`: Application icons and images.
- `static/css/`: Stylesheets for the UI.

## Dependencies

Key dependencies include:
- Electron: Desktop app framework
- bcrypt: Password hashing
- sqlite3: Database engine
- pdfkit, pdf-parse: PDF handling
- exceljs, xlsx: Excel file handling
- mammoth, docx: Word document processing
- tesseract.js: OCR for image text extraction
- natural, node-summarizer: Natural language processing

## Logging

Application logs are saved to a log file located in the user data directory. Logs include info and error messages for debugging and monitoring.

## Backup

The app automatically backs up the database and uploaded files daily to a configured backup directory (`D:\inward-outward-backup`). It retains the latest 3 backups and deletes older ones.

## License

This project is licensed under the ISC License.

## Author

V&R
