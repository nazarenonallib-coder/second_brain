 **target encoding** is any kind of encoding that replaces a feature's categories with some number derived from the target.

A simple and effective version is to apply a group aggregation from Lesson 3, like the mean.

This kind of target encoding is sometimes called a **mean encoding**. Applied to a binary target, it's also called **bin counting**. (Other names you might come across include: likelihood encoding, impact encoding, and leave-one-out encoding.)

An encoding like this presents a couple of problems, however. First are _unknown categories_. Target encodings create a special risk of overfitting, which means they need to be trained on an independent "encoding" split. When you join the encoding to future splits, Pandas will fill in missing values for any categories not present in the encoding split. These missing values you would have to impute somehow.

Second are _rare categories_. When a category only occurs a few times in the dataset, any statistics calculated on its group are unlikely to be very accurate. In the _Automobiles_ dataset, the `mercurcy` make only occurs once. The "mean" price we calculated is just the price of that one vehicle, which might not be very representative of any Mercuries we might see in the future. Target encoding rare categories can make overfitting more likely.

A solution to these problems is to add **smoothing**. The idea is to blend the _in-category_ average with the _overall_ average. Rare categories get less weight on their category average, while missing categories just get the overall average.

In pseudocode:

```
encoding = weight * in_category + (1 - weight) * overall
```

where `weight` is a value between 0 and 1 calculated from the category frequency.

An easy way to determine the value for `weight` is to compute an **m-estimate**:

```
weight = n / (n + m)
```

where `n` is the total number of times that category occurs in the data. The parameter `m` determines the "smoothing factor". Larger values of `m` put more weight on the overall estimate.