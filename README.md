# FlaskML
---
<p>
  This project focuses on using data from dataset in order to predict whether or not an individual will be granted a work visa.
  This project is hosted on pythonanywhere.com, specifically <a href="http://sbosq.pythonanywhere.com/"> here </a>. Working with Flask I was able to get this classification tool online and on a website for access anywhere.
  Before settling on using Flask, I also explored my options with Django. However, ultimately I decided with Flask since Pythonanywhere's servers were more friendly towards Flask. <br>
</p>
<p>
  The following are the steps that I followed to get from a local setup on my local environment, to being able to host this tool on Pythonanywhere's cloud servers.
  <ol>
    <li>
      Download the csv file from Kaggle
    </li>
    <li>
      Explore the downloaded csv file, clean or extract the needed data and storing that in a different csv file for use
    </li>
    <li>
      Using <b><i>Pandas, Sklearn, and joblib</i></b> libraries, I begin by reading the csv file as a pandas Dataframe
    </li>
    <li>
      The csv delimiter and dtype are established and continue by iterating through the items in the Dataframe columns
    </li>
    <li>
      Using MinMaxScaler the values of the cat codes are now limited to a range of 0 to 1. This makes it easier for the algorithm to work and makes the classification report much easier to read/understand
    </li>
    <li>
      In order to train and load different data to test the accuracy of our model, it's crucial to first narrow our attributes to just two. This is accomplished by using two variables to store said attributes in
    </li>
    <li>
      Once are attributes are stored in just two variables, the next step is to use the train_test_split method using the newly created variables which store our attributes values
    </li>
    <li>
      From here a test size needs to be determined in order the best results to be achieved, this can be done manually or by using a predetermined method such as the Elbow Method. Another thing to be done is
      to set the random state of the train test split, this is done to assure that other can repeat the split using the same elements from the data being used
    </li>
    <li>
      Once this is done, the next step is to decide which ML algorithm will be used. It is always a good idea to test out multiple algorithms in order to find the one that best suits the working dataset
    </li>
    <li>
      In order to get a full understanding of how well the algorithm is working, using sklearn.metrics classification_report will give precision, recall, and f1 scores
    </li>
    <li>
      Once satisfied with the results of an algorithm, use <i>joblib</i> to load the <b><i>trained model</i></b> as a pickle. Storing it as a pickle will not only reduce the strain on memory, but it will also help
      load the trained model on cloud servers where storage or available space may be an issues
    </li>
    <li>
      The next step is to load the .pkl and .py files from my computer to the cloud server. Other files needed are .html and .css for the web pages that will be displayed
    </li>
  </ol>
</p>
