# Data-Access-from-Fire-Store
Python code that I developed to access data from fire store and fetch top three preferred  movies of audience

# Firestore
# 1.	Backup Files to Cloud Storage
Use the gsutil command to copy the firestore directory to your Cloud Storage bucket:
Code: gsutil -m cp -r firestore gs://YOUR-BUCKET/firestore
# 2.	Import Documents into Firestore
Use the gcloud CLI to import the documents from the Cloud Storage bucket into Firestore:
Code: gcloud beta firestore import gs://YOUR-BUCKET/firestore
For more details, refer to the Firestore Export and Import Documentation.

This Python script demonstrates how to interact with a Firestore database using the Firebase Admin SDK to retrieve and export movie data. It begins by initializing the Firestore client with a service account key file, allowing the script to authenticate and interact with the database securely. The get_movie_data function retrieves a specific movie document from the movies collection using its unique movie ID. If the document exists, its data is printed to the console; otherwise, an error message is displayed.
The script also includes the get_all_movies function, which streams and prints all documents from the movies collection, providing an overview of all stored movie entries. 
        Additionally, the save_movies_to_csv function exports the data from the movies collection to a CSV file in the specified downloads folder. It uses Python's csv module to write data, including fields like movie ID, title, genres, ratings, and other attributes, into a structured format. This enables easy access and analysis of the movie data outside the Firestore environment.



