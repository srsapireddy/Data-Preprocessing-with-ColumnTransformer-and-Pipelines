# Data-Preprocessing-with-ColumnTransformer-and-Pipelines
Sklearn’s Pipelines with ColumnTransformer is an easy way to apply transformation rules in a standard manner, creating a more organized and clean code. </br>

## ColumnTransformer
What a ColumnTransformer allows is to apply a Sklearn’s Transformer only in a group of columns.</br>
![image](https://github.com/srsapireddy/Data-Preprocessing-with-ColumnTransformer-and-Pipelines/assets/32967087/1384fc26-b5d3-4fd3-a562-316367f00f8c)</br>
The ColumnTransformer object receives a list of tuples composed of the transformer name (this is your choice), the transformer itself, and the columns where to apply the transformation. The argument remainder specifies what needs to be done with all other columns.</br>
![image](https://github.com/srsapireddy/Data-Preprocessing-with-ColumnTransformer-and-Pipelines/assets/32967087/ce5e1bcb-0da4-41b3-b86a-fb5b33744dd1)</br>

## ColumnTransformers with Pipelines
The ColumnTransformer is quite helpful, but more is needed. In many cases, a column needs to be processed in multiple steps.</br>

For example, the numerical feature “price” may require an operation to replace the NULL values with the data mean, a log transformation to distribute the data more symmetrically, and standardization to make its values fall closer to the interval [-1, 1].</br>

With pipelines, we can chain multiple transformers to create a complex process. Because a pipeline object is equivalent to a simple transformer (e.g., it has the same .fit() and .transform() methods), it can be inserted into the ColumnTransformer object.</br>

You can also put a ColumnTransformer inside a Pipeline because it is a simple transformer object, and this loop can go on as long as you need.</br>

![image](https://github.com/srsapireddy/Data-Preprocessing-with-ColumnTransformer-and-Pipelines/assets/32967087/1787be2e-4d8c-451c-a456-44bb19fa1d33)</br>


The pipeline object has quite an intuitive interface. It accepts a list of tuples, each representing a transformer, with a name of your choice and the transformer object itself. It applies the transformations in the specified order.</br>

### Link: https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html



