# Website Pelangi

An interactive web application that demonstrates DOM API manipulation using vanilla JavaScript.

## Features
### 1. **Text Color Picker**
- Select any color using the HTML color input element
- Text color on the page updates in real-time as you pick different colors
- Great for exploring how DOM styling works dynamically

### 2. **Background Image Uploader**
- Upload an image file from your computer
- The image is automatically set as the page's background
- Image is centered, covers the full viewport, and doesn't repeat

## How It Works

### Text Color Change
```javascript
var txtColor = document.getElementById("textColor");
txtColor.addEventListener("input", function(){
    document.body.style.color = txtColor.value;
});
```
- Listens to the color input's "input" event
- Changes the body's text color property to the selected color value

### Background Image Upload
```javascript
fileBg.addEventListener("change", (event) => {
    var doc = event.target.files[0];
    if (doc) {
        var file = new FileReader();
        file.onload = function(e) {
            document.body.style.backgroundImage = `url('${e.target.result}')`;
            // Apply background styling
        };
        file.readAsDataURL(doc);
    }
});
```
- Listens to the file input's "change" event
- Uses the FileReader API to read the selected image
- Converts the image to a data URL
- Applies it as the page's background image

## Technologies Used

- **HTML5** - Page structure and input elements
- **CSS3** - Styling and layout (Flexbox)
- **Vanilla JavaScript** - DOM manipulation and event handling
- **FileReader API** - Image file reading

## Getting Started

1. Open `index.html` in a web browser
2. Use the color picker to change text color
3. Upload an image file to set it as the background
4. Enjoy your custom-styled website!

## File Structure

- `index.html` - Main HTML file with structure and JavaScript
- `style.css` - Styling and layout
- `README.md` - Documentation (this file)
