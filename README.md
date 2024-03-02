# NewsArticles
Inference on News Articles Data 




Qs:

1.4. Does variable selection and model build using same trainning cause overdipping?
2. Does the method used for "3.1.4 Zero-inflated test" appropriate/necessary/correct?
3. Does splitting using population paramter create bias?
# Set seed
set.seed(111)

# Split data - train/test
partition <- createDataPartition(y = news_data$shares, 
                                 p = 0.7,  # Proportion to allocate to training set
                                 list = FALSE)  # Get indices directly

# Create the training and test datasets
training_set <- news_data[partition, ]
test_set <- news_data[-partition, ]

dim(training_set)
dim(test_set)


