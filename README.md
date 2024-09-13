# Image Search Engine

<p>The **Image Search Engine** is a web application designed to allow users to search for images based on a keyword, using the Unsplash API. Built using HTML, CSS, and JavaScript, the app provides a simple and clean interface where users can input a keyword to fetch and display images related to their search query.</p>
<h2>Key Features</h2>
<h3>Image Search Functionality</h3>
<p>The primary feature of the application is its ability to fetch and display images from Unsplash based on the user's keyword search. After the user inputs a keyword and clicks the "Search" button, the app retrieves a set of images and displays them in a grid layout.</p>
<h3>User Interface</h3>
<h4>Search Input</h4>
<p>A single-line text input field allows users to type in a search query. The input field is accompanied by a "Search" button to initiate the image search. The placeholder text guides users on what to input.</p>
<h4>Image Display</h4>
<p>Images are displayed in a responsive grid format, with each image clickable, directing the user to the original Unsplash page for the image. The grid automatically adjusts to different screen sizes, making it visually appealing and functional on various devices.</p>
<h4>Show More Button</h4>
<p>Once the initial set of images is displayed, users can click the "Show more" button to load additional images, enabling continuous scrolling and exploration.</p>
<h3>Visual Design</h3>
<p>The app features a modern, sleek design, using a deep purple background with contrasting elements. The fonts and colors are chosen to provide clarity and a pleasing user experience. The "Search" and "Show more" buttons are highlighted with a bright red color, making them easy to locate and use.</p>
<h3>Responsive Design</h3>
<p>The app is fully responsive, ensuring a smooth user experience on both desktop and mobile devices. The image grid adapts to different screen sizes, and the layout remains clean and accessible.</p>
<h2>Technical Overview</h2>
<h3>HTML Structure</h3>
<p>The HTML structure consists of a header, a form with a search input field and button, a `div` element to display search results, and a "Show more" button. The form submits the search query, and the results are appended dynamically to the `div` element.</p> 
<h3>CSS Styling</h3>
<h4>Background and Fonts</h4>
<p>The application uses the "Poppins" font, giving it a modern and clean aesthetic. The background features a deep blue shade, with white text and vibrant button colors providing contrast.</p>
<h4>Grid Layout</h4>
<p>Images are displayed using a grid layout that dynamically adjusts depending on the screen size. Each image is neatly contained within a rounded border, and the layout ensures a visually appealing display of the search results.</p>
<h3>JavaScript Functionality</h3>
<p>The JavaScript in the app handles the interactivity, including fetching images from the Unsplash API based on user input and dynamically updating the search results on the page.</p>
<h4>API Fetching</h4> 
<p>The application sends an API request to Unsplash using the provided access key. When the user inputs a keyword, it triggers the fetching of images from the API. The results are processed and displayed in the `search-result` element.</p>

    async function searchImages() {
        const url = `https://api.unsplash.com/search/photos?page=${page}&query=${keyword}&client_id=${accessKey}&per_page=12`;
        const response = await fetch(url);
        const data = await response.json();
    
<h4>Image Display and Pagination</h4>
<p>The fetched images are displayed in a grid layout. The "Show more" button increments the page number and fetches additional images, which are appended to the existing results without clearing the current display.</p>

    showMoreBtn.addEventListener("click", () => {
        page++;
        searchImages();
    });

<h2>Conclusion</h2>
<p>The **Image Search Engine** is a user-friendly and responsive web application that leverages the Unsplash API to fetch and display images based on search queries. Its simple interface and clean design make it easy to use, while the "Show more" feature ensures users can continuously explore new images. The use of modern web technologies such as Fetch API, grid layout, and responsive design principles ensures both functionality and aesthetic appeal.</p>
