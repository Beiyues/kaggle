# kaggle
something about kaggle
2022/6/7<br>
1,来翻译翻译下这个页面<br>
2,还是titanic<br>
启示还是那个b站英文视频靠谱<br>
可以从第一个视频的15分钟开始看<br>
6/21
women=train_data.loc[train_data.Sex=='female']["Survived"]
rate_women=sum(women)/len(women)
print("% of women who survived:",rate_women)

train_data[train_data.Sex=="female"]
看到了22.54
from sklearn.ensemble import RandomForestClassifier
y=train_data["Survived"]

features =["Pclass","Sex","SibSp","Parch"]
X=pd.get_dummies(train_data[features])
X_test =pd.get_dummies(test_data[features])

model=RandomForestClassifier(n_estimators=100,max_depth=5,random_state=1)
model.fit(X,y)
predictions=model.predict(X_test)

output=pd.DataFrame({'PassengerId':test_data.PassengerId,'Survived':predictions})

output.to_csv('my_submission.csv',index=False)
print("Your submission was successfully saved")
![E72%WNZ L GR0M0H)(U S8](https://user-images.githubusercontent.com/51742666/173223603-6dbd0659-6527-4cbf-a49a-221c40f946b1.png)
看到37.00
