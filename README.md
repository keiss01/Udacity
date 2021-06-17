{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Disaster Response Pipeline Project\n",
    "\n",
    "#### Description:\n",
    "\n",
    "The purpose of this project is to classify messages by categories.\n",
    "\n",
    "\n",
    "This project contains:\n",
    "\n",
    "1. ETL - process_data.py - which reads data from two csv files, messages & their respective categories, cleans the data and stores it in a SQLite database.\n",
    "\n",
    "\n",
    "2. ML Pipeline - train_classifier.py - which splits the data to train and test sets, builds & tunes and a model to predict the categories of a new message, outputs results on the test set & saves the model.\n",
    "\n",
    "\n",
    "3. Flask App - run.py - which displays statistical visualization of the training data set & displays the predicted categories of an input text.\n",
    "    \n",
    "#### Structure:    \n",
    " \n",
    "```bash\n",
    "├── app\n",
    "│   ├── template\n",
    "│   │   ├── go.html     # classification result page of web app\n",
    "│   │   └── master.html # main page of web app \n",
    "│   └── run.py          # Flask file that runs app  \n",
    "├── data\n",
    "│   ├── disaster_categories.csv #  data to process\n",
    "│   ├── disaster_messages.csv   # data to process\n",
    "│   ├── process_data.py\n",
    "│   └── DisasterResoponse.db\n",
    "├── models\n",
    "│   ├── classifier.pkl          # saved model \n",
    "│   └── train_classifier.py\n",
    "└── README.MD\n",
    "``` \n",
    "\n",
    "#### Instructions:\n",
    "1. Run the following commands in the project's root directory to set up the database and model.\n",
    "\n",
    "    - To run ETL pipeline that cleans data and stores in database\n",
    "        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`\n",
    "    - To run ML pipeline that trains classifier and saves\n",
    "        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`\n",
    "\n",
    "2. Run the following command in the app's directory to run your web app.\n",
    "    `python run.py`\n",
    "\n",
    "3. Go to http://0.0.0.0:3001/\n",
    "\n",
    " \n"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.6.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
