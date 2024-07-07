To tackle these questions, we'll use Plotly Express, which is a high-level interface for creating expressive and interactive plots. Let's go through each question step by step:

Q1. Load the "titanic" dataset using the load_dataset function of seaborn. Use Plotly express to plot a scatter plot for age and fare columns in the titanic dataset.
python
Copy code
import seaborn as sns
import plotly.express as px

# Load the dataset
titanic = sns.load_dataset('titanic')

# Plot scatter plot using Plotly Express
fig = px.scatter(titanic, x='age', y='fare', title='Scatter Plot of Age vs Fare in Titanic Dataset')
fig.show()
Q2. Using the tips dataset in the Plotly library, plot a box plot using Plotly express.
python
Copy code
import plotly.express as px

# Load the tips dataset from Plotly
tips = px.data.tips()

# Plot box plot using Plotly Express
fig = px.box(tips, x='day', y='total_bill', title='Box Plot of Total Bill by Day')
fig.show()
Q3. Using the tips dataset in the Plotly library, Plot a histogram for x= "sex" and y="total_bill" column in the tips dataset. Also, use the "smoker" column with the pattern_shape parameter and the "day" column with the color parameter.
python
Copy code
import plotly.express as px

# Load the tips dataset from Plotly
tips = px.data.tips()

# Plot histogram using Plotly Express
fig = px.histogram(tips, x='sex', y='total_bill', color='day', pattern_shape='smoker',
                   title='Histogram of Total Bill by Sex, Day, and Smoker Status')
fig.show()
Q4. Using the iris dataset in the Plotly library, Plot a scatter matrix plot, using the "species" column for the color parameter. Note: Use "sepal_length", "sepal_width", "petal_length", "petal_width" columns only with the dimensions parameter.
python
Copy code
import plotly.express as px

# Load the iris dataset from Plotly
iris = px.data.iris()

# Plot scatter matrix using Plotly Express
fig = px.scatter_matrix(iris, dimensions=['sepal_length', 'sepal_width', 'petal_length', 'petal_width'],
                        color='species', title='Scatter Matrix Plot of Iris Dataset by Species')
fig.show()
Q5. What is Distplot? Using Plotly express, plot a distplot.
Distplot in Plotly Express is used to plot a distribution plot, which combines a histogram with a smoothed kernel density estimate (KDE).

python
Copy code
import plotly.express as px

# Generate some sample data
import numpy as np
np.random.seed(0)
data = np.random.normal(loc=0, scale=1, size=1000)

# Plot distplot using Plotly Express
fig = px.histogram(x=data, marginal='rug', title='Distplot of Sample Data')
fig.show()
In the example above, marginal='rug' adds a rug plot along the x-axis to show the distribution of individual data points. Adjust the parameters according to your specific visualization needs.
