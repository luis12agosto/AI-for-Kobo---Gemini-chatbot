# Gemini Chatbot for Kobo E-readers

Unlock the power of Google's Gemini AI directly on your Kobo e-reader. This project provides a lightweight, E Ink-friendly chatbot for brainstorming and getting answers on the go, no tablet or phone required.

<!-- Replace with a real screenshot -->

## ✨ Features

* **E Ink Optimized Interface:** High-contrast design with light and dark themes.
* **Accessibility Controls:** Increase or decrease text size and navigate the conversation with fixed buttons.
* **Persistent Memory:** The conversation is saved on the device and loaded when you reopen the chatbot.
* **Format Interpreter:** Converts Gemini's responses (bold, lists, tables, and code blocks) into a readable HTML format.
* **No Dependencies:** Requires no libraries or frameworks, just pure HTML and JavaScript.
* **Private and Secure:** Your API key and conversations are saved locally on your device.

## 💻 Compatible Devices

This chatbot is designed for e-readers with basic, experimental web browsers that lack support for modern JavaScript. It has been developed and tested on a **Kobo Glo HD**, but it should work on a wide range of similar devices.

The key requirement is a browser that can run simple JavaScript (ES5) and is connected to Wi-Fi. This includes models such as:

* Kobo Touch
* Kobo Glo
* Kobo Aura, Aura H2O, Aura ONE
* Kobo Clara HD
* Kobo Nia

It may also work on other e-readers with similar simple browser features (like older PocketBook or Tolino models), though it has not been tested on them.

## 📋 Requirements

* A Kobo e-reader with the "Web Browser" feature (under Beta Features).
* A Wi-Fi connection.
* A Google account.

## 🚀 Setup Guide (Step-by-Step)

Follow these steps to install and configure the chatbot on your Kobo.

### Step 1: Download the File

Download the `GemChatbot.html` file from this repository.

### Step 2: Get Your Google Gemini API Key

This is the most important step. The API key is your personal, free key to use Gemini.

1.  **Go to Google AI Studio:** Open <https://aistudio.google.com/> in your computer's browser and sign in with your Google account.
2.  **Create an API Key:** Click on "**Get API key**" in the left menu, and then click "**Create API key in new project**".
3.  **Copy Your Key:** A long string of text will be generated. Copy it and save it in a safe place.
4.  **Enable the Service (Crucial!):**
    * Go to the **Google Cloud API Library** by clicking this link: <https://console.cloud.google.com/apis/library>
    * In the search bar, type `Vertex AI API` and press Enter.
    * Click on the result and then click the **ENABLE** button. If it's already enabled, you don't need to do anything.

### Step 3: Edit the Chatbot File

1.  Open the downloaded `chatbot-kobo-en.html` file with a simple text editor (like Notepad on Windows or TextEdit on Mac).
2.  Find the following line near the beginning of the `<script>` section:
    ```javascript
    var apiKey = "PASTE_YOUR_GEMINI_API_KEY_HERE";
    ```
3.  **Replace** `PASTE_YOUR_GEMINI_API_KEY_HERE` with the key you copied in the previous step. Make sure the key stays between the quotation marks.
    * **Correct example:** `var apiKey = "AIzaSy...xxxxxxxxxxxxxxx";`
    * **Incorrect example:** `var apiKey = AIzaSy...xxxxxxxxxxxxxxx;` (without quotes)
4.  Save the changes to the file.

### Step 4: Transfer and Run on Your Kobo

1.  Connect your Kobo to your computer with the USB cable.
2.  Drag your modified `chatbot-kobo-en.html` file to the root memory of your Kobo.
3.  Safely eject the device.
4.  On your Kobo, go to **Settings -> Beta features -> Web browser**.
5.  In the address bar, type the local file path and press **Go**:
    ```
    file:///mnt/onboard/chatbot-kobo-en.html
    ```
That's it! The chatbot will load, and you can start using it.

## ⚠️ Security Warning

**NEVER share your `chatbot-kobo-en.html` file with anyone after adding your API key.** Your key is secret and provides access to Google services in your name.
