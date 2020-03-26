## Download Data
``` python, term= True
iris = 'http://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data'
urlretrieve(iris)
df = pd.read_csv(iris, sep=',')
df=pd.DataFrame(df)
```

## Statistics for the date

``` python, term= True
df.info()
attributes = ["sepal_length", "sepal_width", "petal_length", "petal_width", "Classs"]
df.columns = attributes
print (df.describe())
```
![](/image1.jbeg)
## plot a histogram for each numerical attribute
``` python, term= True
df.hist(bins=50, figsize=(20,15))
plt.show()

```
![](/image2.jbeg)
![](/image3.jbeg)