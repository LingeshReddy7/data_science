# data_science
import matplotlib as plt
import pandas as pd
from matplotlib import pyplot as plt
from sklearn import linear_model

df=pd.read_csv("home.csv")
df

%matplotlib inline
plt.xlabel("area (sq ft)")
plt.ylabel("price (u s)")
plt.scatter(df.area,df.price,color='red',marker='*')
plt.plot(df.area,reg.predict(df[["area"]]),color='blue')

reg = linear_model.LinearRegression()
reg.fit(df[['area']],df.price)

reg.predict([[5000]])

reg.coef_

reg.intercept_

reg.predict([[10000]])

d=pd.read_csv("area.csv")
d

p=reg.predict(d)

d["Prices"] = p

d

d.to_csv("p.csv",index=False)
