# Cite Guard

A comprehensive desktop application built with Electron that helps users check citations in academic documents and provides AI-powered analysis through an integrated chat assistant.

## Features

### Core Functionality
- **File Upload Support**: Upload and view content from PDF, DOCX, and TXT files
- **Built-in Citation Checker**: Automatically detect missing or uncited references in academic documents
- **Multiple Citation Styles**: Support for APA, Chicago, and Harvard citation formats
- **AI-Powered Analysis**: Integrated chat assistant for document analysis and citation guidance
- **Report Generation**: Save analysis results as TXT, DOCX, or PDF files

### User Interface
- Modern, responsive design with Tailwind CSS
- Drag-and-drop file upload interface
- Real-time chat with AI assistant
- Markdown-formatted responses with proper heading and bullet point styling
- Cross-platform desktop application

## Installation

### Prerequisites
- Node.js (version 14 or higher)
- npm (comes with Node.js)

## Usage Guide

### Basic Workflow

1. **Upload Document**
   - Drag and drop a PDF, DOCX, or TXT file onto the upload area
   - Or click "Select File" to browse for a file

2. **Edit Content** (Optional)
   - Use the text editor to modify the document content
   - Ensure your References section is included

3. **Select Citation Style**
   - Choose from APA, Chicago, or Harvard from the dropdown menu

4. **Check Citations**
   - Click "Check Citations" to run the built-in citation checker
   - Results will show missing or uncited references

5. **AI Analysis** (Optional)
   - Click the "Cite Guard Assistant" button to open the chat
   - Ask questions about your document or citations
   - Get AI-powered analysis and suggestions

6. **Save Results**
   - Save your analysis results as TXT, DOCX, or PDF files
   - Use the "Save Report" button in the results section

### AI Assistant Features

The Cite Guard Assistant provides:
- Document analysis and citation review
- Formatting suggestions
- Academic writing guidance
- Reference validation
- Style-specific recommendations

**Note**: The AI assistant operates independently from the built-in citation checker, providing complementary analysis.

## Project Structure

```
Cite Guard/
├── main.js              # Electron main process
├── renderer.js          # Client-side logic and UI interactions
├── index.html           # Main application interface
├── about.html           # About page with team information
├── package.json         # Project configuration and dependencies
├── build/               # Application icons
│   ├── icon.ico         # Windows icon
│   ├── icon.icns        # macOS icon
│   └── icon.png         # Linux icon
└── dist/                # Built applications and installers
```

## Technical Details

### Dependencies
- **Electron**: Cross-platform desktop application framework
- **pdf-parse**: PDF content extraction
- **mammoth**: DOCX file parsing
- **docx**: Word document generation
- **marked.js**: Markdown rendering for chat responses
- **Tailwind CSS**: UI styling framework

### Key Components

#### Main Process (`main.js`)
- Application window management
- File system operations
- IPC communication handling
- Native menu and dialog management
- Citation checking logic

#### Renderer Process (`renderer.js`)
- UI event handling
- File upload and processing
- Chat interface management
- Markdown preprocessing and rendering
- AI assistant integration

#### Citation Checking Algorithm
- Author name extraction and matching
- Reference parsing and validation
- Citation style-specific formatting
- In-text citation detection

## Security

The application includes security measures:
- Dependency vulnerability monitoring via `npm audit`
- Override configurations for known security issues
- Regular dependency updates

## Troubleshooting

### Common Issues

1. **Build Errors**
   - Ensure all dependencies are installed: `npm install`
   - Clear cache if needed: `npm cache clean --force`

2. **Windows Build Issues**
   - If encountering symlink errors, enable Developer Mode or run as administrator
   - Clear winCodeSign cache: `Remove-Item -Recurse -Force "$env:LOCALAPPDATA\electron-builder\Cache\winCodeSign"`

3. **File Upload Issues**
   - Ensure files are in supported formats (PDF, DOCX, TXT)
   - Check file size limits

### Development

#### Making Changes
1. Edit source files (`main.js`, `renderer.js`, `index.html`)
2. Rebuild the application:
   ```bash
   npm run dist
   ```

#### Code Structure
- Follow Electron best practices for main/renderer process separation
- Use IPC for communication between processes
- Maintain clean separation between UI and business logic


## License

This project is proprietary software. All rights reserved.

## Support

For technical support or feature requests, please contact the development team.

---


*Cite Guard - Your comprehensive citation checking and academic writing assistant.*
