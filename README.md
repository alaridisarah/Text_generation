# Text generation using LSTM 

Text generation is a subfield of natural language processing(NLP). Works by using advanced NLP methods to analyze existing text and generate new text. There are 2 types of text generating: Character Generation 
and Word Generation.
The model will take as input a list of units (characters or words) and it will predict the next unit.
For example: “Alanoud is a computer science student”
In word generation it will predict:
“Computer science -> student “
In character generation it will predict:
“uter -> s | nce -> s “

Text generator models can be used in many fields, in healthcare, the text generator model can automate report writing to save doctors’ time and improve report consistency. Also, generate weather reports by analyzing large amounts of weather data.

### Dataset 
We used data from kaggle and are loaded by the opendatasets library an English-language dataset [CNN/DailyMail Dataset](https://www.kaggle.com/datasets/gowrishankarp/newspaper-text-summarization-cnn-dailymail) has little over 300,000 distinct news items and highlight sentences. according to reporting from CNN and the Daily Mail, the dataset is divided into three segments: train, validation, and test.
#### Prepare the dataset
In the beginning, we need to clean the text from  punctuation and stop words to ensure that all articles only have a unique word. A stop words is a low-level information in a text; Ntlk library has a collection of stop words.
Then, a pre-processing of the text in NLP includes:
- Tokenization: a token is an atomic unit in the text. The tokenization process splits text into smaller units (word).
- Sequencing: a process to convert the sequence of words to a sequence of numbers.
- Padding: the input of NN have the same size, and to ensure that all input has the same size, we do a padding to each sequence.

### RNN 
Neural networks cannot memorize the previous input. According to this, we will use a Recurrent neural network (RNN). RNN saves the output of the previous node from feeding the next node to predict the output.
 
According to gradient problems, we will use the Long Short-Term Memory Network (LSTM). The difference between RNN and LSTM, RNN uses an activation function in the hidden layer, while LSTM has multiple gates:
-	Input gate: determine what relevant information can be added from the current step.
-	Forget gate: decide which information will need attention or ignore.
-	Output gate: filter the information will be passed to the next state.

### Evaluating the result
Text generation is evaluated through human ratings or automatic evaluation metrics. So, we have published a survey  containing 5 texts generated by the model for a group of people and we get 13 responses to evaluate the results. 

The criteria where:
1.	Is the text readable?
2.	Is the text informativeness?
3.	Is the text correct grammaticality?
4.	Is the text consistent?


At the end, this model must improve by using more data will make the generating doing better and fine tuning the parameter.

## Prepared By 
- Sarah Khalid Alaradi       skmaloridi@sm.imamu.edu.sa
- Reem Alqahtani             Rasalkahtani@sm.imamu.edu.sa
- Norah Alsharhan            Nalsharhan@sm.imamu.edu.sa
