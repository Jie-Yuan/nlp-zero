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
```
