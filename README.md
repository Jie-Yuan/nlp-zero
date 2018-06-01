# nlp-zero
基于最小熵原理的NLP工具包

https://kexue.fm/archives/5597


```python
trie = XTrie()
for i, j in f.templates.items():
    trie[i.words] = j
    
p = Parser(trie, jieba.lcut) # 建立一个解析器

p.parse('< Template')
p.parse('我是周杰伦')
p.parse(u'苏宁是什么呢') 

+---> < Template
|     +---> <
|     +--->  
|     +---> Template
+---> 我(是周杰伦)
|     +---> 我
|     +---> 是(周杰伦)
|     |     +---> 是
|     |     +---> 周杰伦
|     |     |     +---> 周杰伦
+---> 苏宁(是什么呢)
|     +---> 苏宁
|     +---> 是(什么呢)
|     |     +---> 是
|     |     +---> 什么(呢)
|     |     |     +---> 什么
|     |     |     +---> 呢
|     |     |     |     +---> 呢
```
