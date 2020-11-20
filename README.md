Predict whether or not loans acquired by Fannie Mae will go into foreclosure. Fannie Mae acquires loans from other lenders as a way of inducing them to lend more.
## Installation
# Download the data
1. Clone this repo to your computer.
2. Get into the folder using cd loan-prediction.
3. Run mkdir data.
4. Switch into the data directory using cd data.
5. Download the data files from Fannie Mae into the data directory.
6. You can find the data here.
7. You'll need to register with Fannie Mae to download the data.
8. It's recommended to download all the data from 2019 Q1 to 2019 Q3.
9. Extract all of the .zip files you downloaded.
10. On OSX, you can run find ./ -name \*.zip -exec unzip {} \;.
11. At the end, you should have a bunch of text files called Acquisition_YQX.txt, and Performance_YQX.txt, where Y is a year, and X is a number from 1 to 4.
12. Remove all the zip files by running rm *.zip.
13. Switch back into the loan-prediction directory using cd ...
14. Install the requirements
15. Install the requirements using pip install -r requirements.txt.
16. Make sure you use Python 3.
17. You may want to use a virtual environment for this.
## Usage
Run mkdir processed to create a directory for our processed datasets.
Run python assemble.py to combine the Acquisition and Performance datasets.
This will create Acquisition.txt and Performance.txt in the processed folder.
Run python annotate.py.
This will create training data from Acquisition.txt and Performance.txt.
It will add a file called train.csv to the processed folder.
Run python predict.py.
This will run cross validation across the training set, and print the accuracy score.

