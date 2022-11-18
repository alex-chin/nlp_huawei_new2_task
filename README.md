# Assignment 2
## Text multiclass classification: film`s genre

Your task is to classify film descriptions into 6 classes (Horror, Kids, Mystery, Comedy, Action, Drama). The metric is **Accuracy**.

We present you 4 baseline solutions based on logistic regression, catboost, LSTM and Transformers. You can find them in their respective folders: `./baseline_tfidf_logreg`, `./<catboost_baseline>`, `./baseline_rnn` and `./<transformer_baseline>`. Each of these folders contains a file `requirements.txt` that will help you with the installation of the dependencies. To see the score and how many points you get if you can beat him, look at the table below:

| baseline    | Accuracy    | Points      |
| ----------- | ----------- | ----------- |
| LogReg      | 0.41624     | X points    |
| CatBoost    | WIP         | Y points    |
| LSTM        | 0.46319     | Z points    |
| Transformer | WIP         | V points    |

If you will be the first in your group, you'll get 3 bonus points.

Please **DO NOT** develop your solution as a fork of this repository. Also please do not make it publicly available.

### Data

The dataset presented here was collected from one of the public film rating resources. We have selected the 6 most popular movie genres and invite you to try to predict them.

- `train.csv` - The training set, comprising the `movie_name`, `movie_description` and `target` of each film, the latter of which is the genre of the film. `target` comprise the target for the competition. All columns are a string data type.
- `test.csv` - For the test data we give only the `movie_description` of an film together with its `movie_name`.
- `sample_submission.csv` - A submission file in the correct format.

### Evaluation

Submissions are scored using Accuracy error:
$$
Accuracy = \frac{1}{N} \sum_{i=1}^{N} E(y_{true}, y_{pred}),
$$
$$
\mathrm{E}(x, y) = \begin{cases}
    1 & \text{if } x = y \\
    0 & \text{otherwise}
\end{cases},
$$
where $N$ is the number of samples in the test dataset.

### Submission File

For each row in the test set, you need to predict one of the 6 movie genres. The file should contain a header and have the following format:
```
target
Horror
Horror
Horror
Horror
...
```
