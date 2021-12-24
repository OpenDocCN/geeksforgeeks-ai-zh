# Python |用 NLTK 引理

> 原文:[https://www . geeksforgeeks . org/python-lemmati 化-with-nltk/](https://www.geeksforgeeks.org/python-lemmatization-with-nltk/)

引理化是将一个单词的不同屈折形式组合在一起的过程，这样它们就可以作为一个单独的项目进行分析。引理化类似于词干，但它给词带来了语境。所以它把意思相似的词和一个词联系起来。
文本预处理包括[词干化](https://www.geeksforgeeks.org/introduction-to-stemming/)和词汇化。很多时候，人们发现这两个术语令人困惑。有些人把这两个当作一回事。实际上，词条化比词干化更受欢迎，因为词条化可以对单词进行形态学分析。
**引理的应用有:**

*   用于搜索引擎等综合检索系统。
*   用于紧凑索引

```
Examples of lemmatization:

-> rocks : rock
-> corpora : corpus
-> better : good
```

词干的一个主要区别是，引理化采用了一个词性参数“pos”，如果不提供，默认为“名词”
下面是使用 NLTK 的引理化词的实现:

## 蟒蛇 3

```
# import these modules
from nltk.stem import WordNetLemmatizer

lemmatizer = WordNetLemmatizer()

print("rocks :", lemmatizer.lemmatize("rocks"))
print("corpora :", lemmatizer.lemmatize("corpora"))

# a denotes adjective in "pos"
print("better :", lemmatizer.lemmatize("better", pos ="a"))
```

**输出:**

```
rocks : rock
corpora : corpus
better : good
```