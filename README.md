# Attendance Matrix Generator

A beautiful, modern web application for generating comprehensive attendance reports from Excel files. Built for Carnegie Mellon University School of Architecture.

## Features

**Easy to Use**
- Upload Excel files with attendance data
- Add supplemental attendance from paper sign-in sheets
- Automatic date detection and sorting
- Real-time processing in the browser

**Comprehensive Reports**
- Daily attendance matrix (Present/Absent for each class)
- Individual student statistics
- Class-by-class breakdown
- Visual color-coded percentage indicators

**Multiple Export Options**
- Download as Excel (.xlsx)
- Download as CSV
- Fully formatted and ready to use

## How to Use

### 1. Prepare Your Excel File

Your Excel file should have:
- A sheet named `Final AttendanceParticipation` with your student roster
  - Column `Student` for student names
  - Column `Andrew` for student emails
- Individual date sheets (one per class session)
  - Each sheet should have an `Email Address` column
  - Students who attended will have their email in that sheet

### 2. Upload and Process

1. Visit the web application
2. Click "Upload" and select your Excel file
3. (Optional) Add any additional attendance records in the text area
   - Format: `Date Name|Email`
   - Example: `Nov 13 John Doe|jdoe@example.com`
4. Click "Generate Attendance Matrix"

### 3. View Results

The app will display:
- Total students and class sessions
- Average attendance percentage
- Number of students in different attendance ranges
- Full attendance matrix table with color-coded status

### 4. Download

Export your results as:
- **Excel** - Formatted spreadsheet with all data
- **CSV** - Plain text format for easy import

## Deployment to GitHub Pages

### Method 1: Simple Upload

1. Create a new repository on GitHub
2. Name it something like `attendance-matrix`
3. Upload the `attendance-matrix-app.html` file
4. Go to Settings → Pages
5. Select "Deploy from a branch"
6. Choose your main branch and root folder
7. Click Save
8. Your site will be live at: `https://yourusername.github.io/attendance-matrix/attendance-matrix-app.html`

### Method 2: Rename to index.html (Cleaner URL)

1. Rename `attendance-matrix-app.html` to `index.html`
2. Create a new repository
3. Upload the `index.html` file
4. Enable GitHub Pages (Settings → Pages)
5. Your site will be live at: `https://yourusername.github.io/repository-name/`

### Method 3: Using Git

```bash
# Clone your repository
git clone https://github.com/yourusername/attendance-matrix.git
cd attendance-matrix

# Add the file (rename to index.html for cleaner URL)
cp attendance-matrix-app.html index.html

# Commit and push
git add index.html
git commit -m "Add attendance matrix application"
git push origin main

# Enable GitHub Pages in repository settings
```

## Technical Details

### Technologies Used
- **HTML5** - Structure and content
- **CSS3** - Styling with custom properties and animations
- **JavaScript** - Client-side processing
- **SheetJS (XLSX)** - Excel file reading/writing
- **Google Fonts** - JetBrains Mono & Playfair Display

### Browser Support
- Chrome/Edge (recommended)
- Firefox
- Safari
- Any modern browser with ES6 support

### Privacy & Security
- **All processing happens in your browser** - no data is sent to any server
- Your Excel files never leave your computer
- Works completely offline after initial load
- No cookies, no tracking, no data collection

## File Format Requirements

### Main Roster Sheet
Must be named: `Final AttendanceParticipation`

Columns:
- `Student` - Student name
- `Andrew` - Student email (or `Email`)

### Date Sheets
Each class session should have its own sheet with:
- Any name (will be auto-detected by timestamp)
- Column `Email Address` with student emails who attended
- (Optional) `Timestamp` column for automatic date detection

### Additional Attendance Format
For manual entry in the text area:

```
Nov 13 John Doe|jdoe@andrew.cmu.edu
Nov 13 Jane Smith|jsmith@andrew.cmu.edu
Dec 05 John Doe|jdoe@andrew.cmu.edu
```

Each line: `Date Name|Email`

## Customization

You can easily customize the appearance by editing the CSS variables at the top of the file:

```css
:root {
    --primary: #1a1a2e;      /* Main background */
    --secondary: #16213e;     /* Secondary background */
    --accent: #0f3460;        /* Accent color */
    --highlight: #e94560;     /* Primary highlight */
    --success: #06d6a0;       /* Success/present color */
    --warning: #ffd166;       /* Warning/medium color */
    --danger: #ef476f;        /* Danger/absent color */
}
```

## Troubleshooting

**Problem: File won't upload**
- Ensure your file is in .xlsx or .xls format
- Check that the file isn't corrupted
- Try a different browser

**Problem: No dates detected**
- Ensure date sheets have an `Email Address` column
- Check that the main sheet is named `Final AttendanceParticipation`
- Verify sheets aren't empty

**Problem: Students missing**
- Check that the main roster has `Student` and `Andrew` (or `Email`) columns
- Ensure email addresses match exactly between roster and date sheets
- Look for typos in email addresses

## Support

For issues or questions:
1. Check the instructions above
2. Review your Excel file format
3. Try with a different browser
4. Contact: [Your contact information]

## License

Created for Carnegie Mellon University School of Architecture
Free to use and modify for educational purposes

## Credits

Built by Ananya
Carnegie Mellon University School of Architecture
December 2025

---

**Note**: This application runs entirely in your browser. Your data stays private and secure on your device.
