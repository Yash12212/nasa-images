# ✨🚀 NASA Image & Video Gallery 🌠✨

**Explore the Cosmos from Your Browser!**

Welcome to a sleek, single-page web application that beams NASA's Astronomy Picture of the Day (APOD) directly to you. Discover breathtaking images and captivating videos, save your favorites, and dive deeper into the wonders of space. All within a single HTML file!

---

## 🌟 Stellar Features 🌟

*   🌌 **Cosmic Feed:** Fetches and displays a curated selection of recent/random media from the NASA APOD API.
*   🎬 **Multimedia Ready:** Seamlessly handles both stunning space images and informative videos.
*   👁️‍🗨️ **Detailed Deep Dive:** A clean modal overlay lets you:
    *   View media in a larger format.
    *   Read the full, fascinating description.
    *   Link directly to high-resolution images (when NASA provides them!).
    *   Watch embedded YouTube & Vimeo videos without leaving the app.
*   ❤️ **Personal Collection (Favorites):**
    *   Bookmark your most-loved space discoveries with a simple click.
    *   Your favorites are saved *locally* in your browser's storage. 💾
    *   Easily filter to see *only* your treasured collection.
*   📱 **Adapts to Your Viewport:** Fully responsive design ensures a great experience on desktops, tablets, and phones.
*   🔗 **Share the Wonder:** Basic Twitter & Facebook sharing options built into the detail view.
*   ⏳ **Smooth Experience:** Visual cues for loading states and clear error messages guide your journey.
*   ⬆️ **Quick Ascent:** A handy "Scroll to Top" button zooms you back to the controls.
*   🌕 **Fullscreen Immersion:** View images or videos distraction-free using the fullscreen mode in the modal.
*   ♿ **Accessible Design:** Foundational accessibility features (ARIA, focus management) are included.

---

## 🚀 Lift Off! (How to Use) 🚀

This app is pure client-side magic – no build steps needed! But due to browser security around API calls (`fetch`), you need to serve it, not just open the file.

1.  **Download:** Grab the `index.html` file (or whatever you named it).
2.  **Serve Locally:** Open your terminal/command prompt *in the same directory* as the file and run a simple local server:
    *   **Python 3:** `python -m http.server`
    *   **Python 2:** `python -m SimpleHTTPServer`
    *   **Node.js (if you have `http-server` installed globally):** `http-server`
    *   *(Or use any other local server tool you prefer!)*
3.  **Navigate:** Open your web browser and go to the address provided by your server (usually `http://localhost:8000` or similar).
4.  **Explore!**
    *   Hit `Show Latest` to fetch cosmic goodies.
    *   Click the `<i class="fas fa-heart"></i>` (heart icon) on cards to favorite/unfavorite.
    *   Use `Show Favorites` to see your saved items.
    *   Click `View Details` (or the media itself for videos) to open the modal.

---

## ⚙️ Power Up (Configuration) ⚙️

Tweak the app's behavior directly in the `<script>` tag near the bottom of the HTML:

```javascript
const CONFIG = {
    // IMPORTANT: Replace DEMO_KEY for better performance!
    API_KEY: 'DEMO_KEY', // Get your own FREE key: https://api.nasa.gov/
    BASE_URL: 'https://api.nasa.gov/planetary/apod', // The mothership API
    RANDOM_COUNT: 6,      // How many items to fetch at once
    ANIMATION_DELAY: 70,  // Card entrance animation stagger (ms)
    FADE_DURATION: 300,   // Generic fade speed (ms) - used subtly
    LOCAL_STORAGE_KEY: 'nasaGalleryFavoritesV2', // Browser storage ID for faves
    DEBOUNCE_DELAY: 150,  // Scroll event optimization (ms)
};
