# backend-test-assignment

1. Upload csv list from example.csv file to Google Storage and create function handler (https://firebase.google.com/docs/functions/gcp-storage-events)
2. Parse it and create document in firestore which describes general information about uploaded list, and subcollection of documents where each row from csv will be as separated document
3. Trigger PubSub events (using [@google-cloud/pubsub](https://googleapis.dev/nodejs/pubsub/latest/index.html)) for each document of subcollection described above, and create listeners for them
4. In listener function process document which has row from previously uploaded list and find all phone numbers
5. Make API request to lookup each phone number which were found in document to specific API (for example [veriphone.io](https://veriphone.io/)) and save results for valid phone numbers
6. Mark document which describes whole list as processed

## Requires
  - Use TypeScript
  - Your code should be sent via Pull Request

## Tips
  - Create own project on [firebase](https://firebase.google.com/)
  - Use firebase [emulator](https://firebase.google.com/docs/emulator-suite) for local development 
  - Create free account on [veriphone.io](https://veriphone.io/)
