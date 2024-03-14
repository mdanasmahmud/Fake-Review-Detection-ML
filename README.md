# Fake-Review-Detection-ML

Model is mainly created to detect fake reviews using tensorflow framework. 
The columns can be fully customizable for training any CSV files and the parameters are well configured by default.
Lastly the repository has two files, the model itself and the preprocessing steps

# Pre Processing:

- Text summarizer to fit long text into bert models.
- Converting profile links to unique user ID for detecting duplicate users.
- Deleting empty rows and converting the overall score to labels.
- Other features such as lower case, emoji conversion, remove Punchuation, remove stopwords.
- Lastly for removing outliers using IQR method.

# Model:

- Used latest version of ConvBert as it is better than Bert for multispace context undertanding.
- Used one hot encoding for label tranlation as categorical crossentropy was used.
- Created a customized convBert tokenizer for converting text to tokens.
- Numerical columns were seperated into a different layer for further processing.
- Used stacked BiLSTM on features extracted from the convBert layer.
- Used other parameters to avoid overfitting such as dropout layers, regulizers with proper learning rate.
- Lastly for training used early stopping and reducePlatueOnLR for dynamic learning rate conversion.
