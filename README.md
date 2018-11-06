# song的方案

Practical Techniques for Searches on Encrypted Data这篇文章的代码实现
使用Python 2.7.
需要PyCrypto库
```
pip install PyCrypto
```

## Usage

把输入的文档放在`/raw`下再运行代码，会把所有输入文件加密并且放入到`/ciphertext`中。

输入关键字，会在加密的文档中查找含有这个关键字的文档，并把所有情况（是否含有）打印出来。

下面是一个实例：

```
$ python scheme.py 

Enter a word to search: tarantula
Not present in input0.enc
Present in input1.enc

Enter a word to search: rooster
Present in input0.enc
Not present in input1.enc

Enter a word to search: this
Present in input0.enc
Present in input1.enc

Enter a word to search: lion
Not present in input0.enc
Not present in input1.enc

Enter a word to search:  // Press Ctrl+D to exit
Quitting...

$ 
```

点击这里下载论文 
##[Practical Techniques for Searches on Encrypted Data](http://www.cs.berkeley.edu/~dawnsong/papers/se.pdf)

by Dawn Xiaodong Song, David Wagner, and Adrian Perrig.

In this paper, the authors develop a set of algorithms that allow searches 
over encrypted data. These algorithms provide a linear search (O(n)) for each
document and introduce relatively little space overhead. Proofs of the security
of their model are also included which show that the server the data is hosted
on “cannot learn anything about the plaintext given only the ciphertext”.
