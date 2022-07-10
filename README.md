# Analysis of Dating profiles: A Machine Learning Approach

Clustering and creating a recommendation algorithm:

The scope for this part of the project was to cluster the user’s profiles into groups and to try to find a match more easily with the help of machine learning algorithms. We tried using different modelling/training methods for the data we had. The first step was to clean and preprocess the available data in a way it can be understood by the algorithms.

The preprocess consisted of splitting the data into numerical (age, income, height) and categorical variables (diet, education, job). Then the numerical variables were scaled using standardscaler and the categorical variables were transformed from string to float using ohehotencoder.

Kmeans clustering algorithm was chosen to cluster the profile data into different groups. The results from kmeans were plotted and the elbow plot showed 7 clusters. And when further investigated using a cluster plot , it was noted that there are no distinct clusters.

Feature reduction was done using PCA, and the elbow plot showed 7 clusters, and the cluster plot were better distinct than before.

The clusters were added to the original dataset. Then proceeded with training the model using supervised Machine Learning algorithm. K nearest neighbour and random forest methods were tested for this purpose. The accuracy score for the KNN method was 63% and 55% for training and testing data respectively. However, on the other hand randomforest model gave a very good score of above 95% for both training and testing data.

Now that the model is trained, a pipeline was created to be used as the basis for processing data, clustering the new user profile and ultimately for recommendation system to work. The model was saved in a pickle file and this loads the pipeline when there is new test data available.

# Webpage:
A basic webpage was designed using HTMl, CSS and Bootstrap,which was made interactive using a Flask application.
The Model building page shows the overview of the machine learning algorithms used, elbow graphs, cluster plots and the pipeline created.
The Model testing page includes a basic form for users to input details, similar to the one used by the dating applications. Basic profile information can be filled out in the form and when the Match me button is clicked the pipeline is loaded in the background that predicts the cluster that the user falls into and pulls 5 random profiles information from the OkCupid dataset and shows it as a table, which is similar to the way dating app works.
