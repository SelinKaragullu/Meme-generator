


# 🤪 Meme Generator

A interactive React application that allows users to generate custom memes. It fetches a database of popular meme templates from an API and allows users to add their own top and bottom text in real-time.


<h2> Gif </h2>


![Meme generator](https://github.com/user-attachments/assets/6cb2ee89-8268-43e2-9fa2-89c75a424cab)

## ✨ Features

* **API Integration:** Fetches the top 100 popular memes from the [Imgflip API](https://imgflip.com/api) on initial load.
* **Randomizer:** A button to randomly select a new meme template from the fetched data.
* **Real-time Editing:** Input fields for "Top Text" and "Bottom Text" instantly update the meme image overlay.
* **Responsive Design:** Styled with custom CSS, Grid layouts, and Google Fonts (Karla) for a clean user interface.

## 🛠️ Built With

* **React 19** - JavaScript library for building user interfaces (Release Candidate version).
* **Vite** - Next Generation Frontend Tooling for fast development servers.
* **CSS3** - Custom styling including linear gradients and text shadows.

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

* Node.js (Version 18 or higher recommended)
* npm (comes with Node.js)

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/yourusername/meme-generator.git](https://github.com/yourusername/meme-generator.git)
    cd meme-generator
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Start the development server**
    ```bash
    npm run dev
    ```

4.  Open your browser and navigate to the local host URL provided by Vite (usually `http://localhost:5173`).

## 🧠 How It Works

The core logic lives in `Main.jsx`. Here is a breakdown of the key concepts used:

* **`useEffect` Hook:** Used to perform the side effect of fetching data from the API when the component first renders.
    ```javascript
    useEffect(() => {
        fetch("[https://api.imgflip.com/get_memes](https://api.imgflip.com/get_memes)")
            .then(res => res.json())
            .then(data => setAllMemes(data.data.memes))
    }, [])
    ```

* **`useState` Hook:** Manages the state of the current meme (image URL and text) as well as the array of all available memes.
    ```javascript
    const [meme, setMeme] = useState({
        topText: "One does not simply",
        bottomText: "Walk into Mordor",
        imageUrl: "[http://i.imgflip.com/1bij.jpg](http://i.imgflip.com/1bij.jpg)"
    })
    ```

* **Controlled Components:** The `handleChange` function updates the state object dynamically based on the input's `name` property, ensuring the UI stays in sync with the state.

## 📂 Project Structure

```text
├── src
│   ├── assets
│   │   └── troll-face.png  # Header Icon
│   ├── App.jsx             # Main Application Wrapper
│   ├── Header.jsx          # Top Navigation Bar
│   ├── Main.jsx            # Core Logic, Form, and Image Display
│   ├── index.css           # Global Styles
│   └── index.jsx           # Entry Point
├── index.html              # HTML Template
├── package.json            # Dependencies and Scripts
└── vite.config.js




