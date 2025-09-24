# PDF Viewer with Blank Page Insertion

A modern, client-side PDF viewer that allows you to preview PDF documents and insert blank pages at any position, then download the modified PDF while preserving original quality and searchability.

🌐 **Live Demo**: [https://split-pdf-by-review.netlify.app/](https://split-pdf-by-review.netlify.app/)

## ✨ Features

### 🎯 Core Functionality
- **PDF Preview**: View PDF documents in a clean, grid-based interface
- **Blank Page Insertion**: Add blank pages after any existing page
- **Quality Preservation**: Maintains original PDF quality and searchability
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Client-Side Processing**: No server uploads - everything happens in your browser

### 🎨 User Interface
- **4-Column Grid Layout**: View up to 4 pages per row on desktop
- **Responsive Grid**: Automatically adjusts to 3, 2, or 1 column based on screen size
- **Modern Design**: Clean, card-based layout with subtle shadows and rounded corners
- **Intuitive Controls**: Easy-to-use buttons for adding blank pages

### 🔧 Technical Features
- **Zero Quality Loss**: Uses PDF-lib for direct page copying (no image conversion)
- **Searchable Text**: Preserves all text content and searchability
- **Vector Graphics**: Maintains charts, diagrams, and vector elements
- **Proper Serialization**: Maintains exact page order as displayed
- **Memory Efficient**: Processes PDFs without server uploads

## 🚀 How to Use

### 1. Upload PDF
- Click the file input area or drag and drop a PDF file
- The PDF will load and display in a 4-column grid layout

### 2. Add Blank Pages
- Click "Add blank page after this" on any page
- Blank pages will be inserted immediately after the selected page
- The page order is maintained exactly as displayed

### 3. Download Modified PDF
- Click the green "💾 Download Modified PDF" button
- The new PDF will download with the filename: `[original_name]_with_blank_pages.pdf`

## 🛠️ Technical Details

### Libraries Used
- **PDF.js** (v2.14.305): For PDF rendering and display
- **PDF-lib** (v1.17.1): For PDF manipulation and creation

### Browser Compatibility
- Modern browsers with ES6+ support
- Chrome, Firefox, Safari, Edge
- Mobile browsers (iOS Safari, Chrome Mobile)

### File Size Limits
- Limited by browser memory (typically 50-100MB PDFs work well)
- No server-side processing means no file size restrictions from hosting

## 📱 Responsive Design

| Screen Size | Columns | Layout |
|-------------|---------|--------|
| Desktop (>1200px) | 4 columns | Full grid view |
| Tablet (900-1200px) | 3 columns | Compact grid |
| Mobile (600-900px) | 2 columns | Stacked layout |
| Small Mobile (<600px) | 1 column | Single column |

## 🔍 Quality Preservation

### What's Preserved
- ✅ **Text Content**: All text remains searchable and selectable
- ✅ **Vector Graphics**: Charts, diagrams, and shapes stay crisp
- ✅ **Fonts & Formatting**: Original fonts, colors, and styling
- ✅ **PDF Structure**: Bookmarks, metadata, and document properties
- ✅ **File Size**: No unnecessary bloat from image conversion

### How It Works
1. **Original Pages**: Copied directly from source PDF using `copyPages()`
2. **Blank Pages**: Created as proper PDF pages with matching dimensions
3. **No Conversion**: Never converts to images, maintaining vector quality

## 🎯 Use Cases

### Document Review
- Add space for handwritten notes
- Insert comment pages between sections
- Create space for signatures or approvals

### Presentation Preparation
- Add blank slides for Q&A sessions
- Insert divider pages between topics
- Create space for live annotations

### Printing & Binding
- Add blank pages for physical binding
- Insert separator pages
- Create space for additional content

## 🚀 Getting Started

### Local Development
1. Clone or download the repository
2. Open `index.html` in a web browser
3. No build process or dependencies required

### Deployment
- Upload `index.html` to any web hosting service
- Works with GitHub Pages, Netlify, Vercel, or any static hosting
- No server-side requirements

## 📄 File Structure

```
pdfviewer/
├── index.html          # Main application file
└── README.md           # This documentation
```

## 🔧 Customization

### Styling
All styles are contained within the `<style>` tag in `index.html`. You can easily customize:
- Colors and themes
- Grid layout (change from 4 columns)
- Page container styling
- Button appearance

### Functionality
The JavaScript is modular and well-commented. You can extend it to:
- Add different page types (not just blank)
- Implement page deletion
- Add page reordering
- Include page annotations

## 🐛 Troubleshooting

### Common Issues
1. **PDF won't load**: Ensure the file is a valid PDF
2. **Blank pages not inserting**: Check browser console for errors
3. **Download not working**: Ensure pop-ups are allowed for downloads

### Browser Console
The application logs page order information to the console:
```
PDF generated with pages in order: ['Page 1', 'Blank', 'Page 2', 'Page 3']
```

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📞 Support

For issues or questions:
- Check the browser console for error messages
- Ensure you're using a modern browser
- Try with a smaller PDF file if experiencing memory issues

---

**Live Demo**: [https://split-pdf-by-review.netlify.app/](https://split-pdf-by-review.netlify.app/)

*Built with ❤️ for seamless PDF editing*