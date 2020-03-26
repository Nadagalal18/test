## Some Statistics For The Date

``` python, term= True
iris = 'http://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data'
urlretrieve(iris)
df = pd.read_csv(iris, sep=',')
df=pd.DataFrame(df)
df.info()
attributes = ["sepal_length", "sepal_width", "petal_length", "petal_width", "Classs"]
df.columns = attributes
print (df.describe())


df.hist(bins=50, figsize=(20,15))
plt.show()

```