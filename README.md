# Gemini_NodeJs_API

<img width="844" alt="Screen Shot 2024-06-25 at 1 57 42 PM" src="https://github.com/Ehye-tech/Gemini_NodeJs_API/assets/63075203/2e0162a9-8dbb-4cc9-8af7-741d056df488">

**Description**

This microservice API provides a backend for your application, utilizing Node.js to handle requests and interact with Gemini, a large language model from Google AI. It offers functionalities to generate text based on user-provided prompts.

**Installation**

1. **Prerequisites:**
   - Node.js (version X.X.X or later) and npm (or yarn) installed on your system. You can check these versions by running `node -v` and `npm -v` (or `yarn -v`) in your terminal.
   - (Optional) A code editor or IDE of your choice for development.
2. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/your-repository-name.git
   cd your-repository-name
   ```
3. **Install Dependencies:**
   ```bash
   npm install  # or yarn install
   ```

**Usage**

1. **Start the Server:**
   ```bash
   node server.js  # Replace with your main application file if different
   ```
   This will start the Node.js server and make your API endpoint accessible.

2. **API Endpoint:**

   - **POST /generate**
     - Description: Sends a prompt to Gemini and returns the generated text.
     - Request Body: JSON object containing a `prompt` property specifying the text to generate.
     - Response: JSON object containing the generated text property (`text`).

   **Example Request:**

     ```json
     {
       "prompt": "Write a poem about a cat."
     }
     ```

   **Example Response:**

     ```json
     {
       "text": "The purring prince, with eyes of gold,  \nStrolls through the house, a story told.  \nHis velvet paws, on silent tread,  \nA fluffy king, upon his bed."
     }
     ```

3. **Client-Side Integration:**

   You can integrate this API with your frontend application or other components using HTTP libraries like Axios or Fetch. Send a POST request to `/generate` with the prompt data in the request body. Parse the JSON response to retrieve the generated text.

**Configuration**

**API Key:**

- This API uses a Google Generative AI API key for accessing Gemini. You'll need to create a project and enable the Google Generative AI API in the Google Cloud Console to obtain an API key.
- Store the API key securely as an environment variable named `API_KEY`. You can use tools like `.env` files or system environment variables for this purpose.

**CORS:**

- By default, this API allows requests from all origins using `cors({ origin: '*' })`. Update this configuration for production environments to restrict access to authorized origins.
  
**Additional Notes**

- This API relies on Google Cloud Platform access and an API key. Refer to Google's documentation for details on setting up your project and API access.
- Consider security best practices for storing and managing API keys.
