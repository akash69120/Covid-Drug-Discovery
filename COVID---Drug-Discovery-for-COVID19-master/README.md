# COVID---Drug-Discovery-for-COVID19
The objective is to prepare a machine learning model that can be used to propose potential novel effective drugs to fight SARS-CoV-2, the virus responsible for COVID-19.


Dataset info:
SARS-CoV-2 virus contains proteins responsible for action and replication of the virus. The protein functions can be stopped by introducing drug molecules that are capable of blocking the protein. In other words, preparation of a drug involves finding molecules that can effectively bind to the protein i.e have a high binding affinity.
In this task, you are provided with a dataset of drug molecules and their binding affinity towards SARS-CoronaVirus Main Proteaese(Mpro), one of the proteins in the target virus.
The data has been generated using Protein-Ligand docking.



SMILES Representation of Molecules -

SMILES are character strings to represent drug molecules. For example, a carbon atom can be represented as “C”, an oxygen atom can be represented as “O”, double bond by “=”. The molecule Carbon dioxide is represented as “C(=O)=O”. Read more about SMILES here - https://en.wikipedia.org/wiki/Simplified_molecular-input_line-entry_system
The max length of the string is 25


Files provided in dataset:
train.csv - (9000 samples) File that should be used for training purpose by the user.
test.csv - (2500 samples) File that will be used for actual evaluation for the leaderboard score.
sample_submission - Just to give an idea about how the output csv file should be.



Assumptions:

1)Path used is Absolute path

2)Python version : Python 3.1

3)Environment : Google colab

4)Installing mol2vec library for assignment purpose.Link is provided in the code.

5)We load trained mol2vec which is trained on Morgan fingerprints with radius = 1 to yield 300 dimensional embeddings.
Link to load trained mol2vec  => https://www.kaggle.com/vladislavkisin/tutorial-ml-in-chemistry-research-rdkit-mol2vec (Can find it at bottom of the kernel in zipped format under name 'model_300dim.pkl')


Steps:

1)We use RDkit for our various conversions. Using Rdkit mol is formed from 'smiles' format for our training and testing purposes.

2)Constructing the sentences from mols.

3)Extracting the embeddings.

4)We split the data into train and validate and analyze with various different regression algorithms like Ridge,svm,lasso,etc and also with their different parameters

5)And eventually the best algorithm is picked and applied on test data.
