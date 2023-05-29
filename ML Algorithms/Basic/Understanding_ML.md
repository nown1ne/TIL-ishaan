# Framework for spotting and solving problems with ML:
## Make Multimedia Searchable
- Handle ,Search and deal with complicated Data types
  - Video
  - Audio
  - Image's
  - PDF's
### Example Project 
- Create a AI Powered Family Video Archive:
<img width="662" alt="Screenshot 2023-05-29 at 5 14 27 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/af98b807-a990-4d9e-83b1-802182ef6c34">

- Upload all vids to Google Cloud Storage
- Video Intelligence API (ML Model / Google Cloud Tool for analysing Video)
  - Transcribes the Video
  - Recognizes any Text on Screen
  - Uses Computer Vision Model to see what is going on in a video
- Search for the keywords and it finds the video's with the help of tag's associated with each video

## Understand Language:
### Semantic Search:
  - Making Machines understand that various different phrases but have the same sentiment (yawning on video, i'm tired)
### Embedding: (To solve the semantics issue)
  - An embedding is a relatively low-dimensional space into which you can translate high-dimensional vectors. Embeddings make it easier to do machine learning on large inputs like sparse vectors representing words. 
  - Ideally, an embedding captures some of the semantics of the input by placing semantically similar inputs close together in the embedding space.(Flying broomstick and Jetpack are close)
  - An embedding can be learned and reused across models.

<img width="701" alt="Screenshot 2023-05-29 at 5 21 34 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/cdfa27ae-debc-4755-a3af-f4ae252b37ee">

## Convert Between Data Types:
- PDF to Audio 
  - AutoML Vision (Identify Sections):
    - analysis the different Blocks of the Pdf (Title, Subtile, Body, Header)
  - Vision API (Extracts Text):
    - Convert the image into Text
  - Text to Speech API:

- Translate Audio to another Language:
<img width="602" alt="Screenshot 2023-05-29 at 5 30 34 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/9a656cda-84a5-40d4-9328-3bf3dc0e9d82">

# Types of Machine Learning:
## Supervised Learning:
- Machine Learns under Guidance (Techer Student)
- Machine learn by feeding them labelled data
  - Specifing how the input and output should look like
- Used to solve:
  - Classification Problems:
    - Predicting a Label or a Class (Email Sorting: Spam and Not-Spam)
  - Regression Problems:
    - Predicting a continuous Quantity (Person's Weight, Stock)
- Forcast Outcomes

## Unsupervised Learning:
- Machine Learns without any direction (Self Study)
- No lables or Guides provided, Machine has to find hidden patterns to make predictions about the output
- Used to solve:
  - Associations Problems:
    - associations of items which frequently co-occur
  - Clustering Problems:
    - Targeted Marketing 
- Discover Underlying Patterns

## Reinforcement Learning:
- To establish or encourage a pattern of Behaviour (Hit And Trail Method)
- Machine interacts with its environment by producing actions and discovers errors or rewards
- Input depends on actions being taken (No predefined Data provided)
- Learn Series of actions
- Used in Self Driving Cars, gaming.

### Output Feedback: 
<img width="1106" alt="Screenshot 2023-05-29 at 5 56 26 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/4669b171-d954-4bdd-b412-8038983e93b1">

