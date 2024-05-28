# Contradictory-My-Dear-Watson

Contradictory, My Dear Watson
Detecting contradiction and entailment in multilingual text using TPUs

https://www.kaggle.com/competitions/contradictory-my-dear-watson/overview

Dataset Description:
The task at hand concerns Natural Language Inferencing (NLI), more especially text entailment. Participants create an NLI model that can identify sentences (0 for entailment, 1 for neutral, and 2 for contradiction) given pairs of sentences that each contain a premise and a hypothesis. The competition intends to investigate whether machines are capable of efficiently identifying logical connections between phrases, which has important ramifications for text analysis, fact-checking, and the detection of fake news.

For this challenge, a dataset with text in fifteen different languages is offered. The task at hand is to create models that, in a variety of linguistic settings, can reliably anticipate the connection labels between pairs of premises and hypotheses. In order to effectively tackle this NLP problem, participants are advised to make use of the potent hardware accelerators known as Tensor Processing Units (TPUs).

A unique identifier for each data instance, {premise} (the first text serving as a basis for comparison), hypothesis} (the second text being compared to the premise),lang_abv} (language abbreviation), language} (full language name), andlabel} (the label indicating the logical relationship between the premise and hypothesis) are among the columns that make up the dataset. The values of 0, 1, or 2 for the {label} represent entailment, neutrality, and contradiction, respectively.

This multilingual dataset provides a real-world scenario where NLI models must handle a variety of linguistic patterns and relationships.

Data Visualization

![image](https://github.com/sandeep822/Contradictory-My-Dear-Watson/assets/50867031/e72ddecc-2679-45b0-8e8f-f10feae004f3)

Multi Model

![image](https://github.com/sandeep822/Contradictory-My-Dear-Watson/assets/50867031/de9aa7a4-212d-4a53-b573-23252687637f)

RNN model Using Keras

Recurrent Neural Network (RNN) for Natural Language Inference using TensorFlow and Keras. The model architecture consists of an LSTM layer with 64 units, followed by a Flatten layer and two dense layers with 128 units and 3 units (for softmax activation corresponding to the three classes: entailment, neutral, and contradiction), respectively. The training is conducted for five epochs with a batch size of 64, and the model's performance is tracked using accuracy as the evaluation metric.

![image](https://github.com/sandeep822/Contradictory-My-Dear-Watson/assets/50867031/ff7ff425-6f27-482f-9455-f3e18f6b7ae8)

Hyperparameter Tuning (Random Forest):

![image](https://github.com/sandeep822/Contradictory-My-Dear-Watson/assets/50867031/27668af9-5031-48aa-8064-b54016c49e5a)

The grid search results for Random Forest hyperparameters are visualized in the plot, where each line corresponds to a specific value of 'n_estimators,' 'max_depth,' or 'min_samples_split.' The x-axis represents the index of hyperparameter combinations, ranging from 0 to 5. For 'n_estimators,' the plot displays three lines corresponding to values of 50, 100, and 200. Similarly, 'max_depth' is represented by lines for 'None,' 10, and 20, while 'min_samples_split' has lines for 2, 5, and 10. The y-axis denotes the mean cross-validated accuracy, providing insights into the performance of each hyperparameter configuration. The visual representation allows for a quick assessment of how changes in these hyperparameters influence model accuracy, aiding in the identification of optimal settings for the Random Forest model in the context of Natural Language Inference.




