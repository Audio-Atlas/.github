<div align="center">
<img src="https://audio-atlas.github.io/audio-atlas-frontend/imgs/AALogo.png" height=100 />
  <h1>Audio Atlas</h1>
  <h2>A fuzzy search tool for sound effects</h2>
  <a href="https://audio-atlas.github.io/audio-atlas-frontend/">Audio Atlas Website</a>
</div>

## About
Audio Atlas is a fuzzy search tool for sound effects. It takes in text query and returns a list of sound effects that match the query. The core of Audio Atlas is the CLAP (Contrastive Language-Audio Pretraining) model made by LAION-AI.
### How does it work?
Here's a simple diagram to explain how Audio Atlas works:

<img src="https://audio-atlas.github.io/audio-atlas-frontend/imgs/diagram.png" height=400/>

### Preprocessing
Audio Atlas preprocesses the existing sound effects data by saving the sound data in a format that is easy to search through. The sound data is then converted into vector embeddings using CLAP's Audio Encoder.

### Query
When a user enters a query, Audio Atlas preprocesses the query and converts it into a vector embedding using CLAP's Text Encoder which has the same dimension as the sound embeddings. It is then compared with the sound embeddings to find the most similar sound effects.

The sound effects are then ranked based on their similarity to the query and passed through a pagination algorithm to return the most relevant sound effects.

### Download
When a user clicks on a sound effect, Audio Atlas fetches the sound effect from the server based on its ID and plays it for the user. The user can then download the sound effect if they like it.

### Technologies Used
Audio Atlas is built using the following technologies:

Frontend: Nuxt (Vue)
Backend: Poetry and Flask


## Set up
To run the app, clone the backend repository and build it using the Dockerfile provided. Configure the .env file to use the appropriate values for your setup. When running the container make sure to set a path to the bind mount where the audio data is stored.
To run the frontend, clone the frontend repository and build it using the provided npm commands.
