Merkle Tree
=
Merkle Tree（默克尔树），也被称为哈希树，是一种树形数据结构，用于有效地验证大量数据的完整性和一致性。名称来自于德国计算机科学家Ralph Merkle。

![image](https://github.com/yxh1120/Homework-group-41/blob/main/Project%2005/2.png)

**默克尔树的结构：**  
叶节点（Leaf Nodes）：表示待校验的数据块，通常是文件或数据块的哈希值。  
内部节点（Internal Nodes）：由两个子节点的哈希值组成，通过将子节点的哈希值连接起来并计算其哈希得到。  
根节点（Root Node）：是最终的哈希值，代表整个默克尔树的完整性。  

**构建过程：**  
将待校验的数据划分为固定大小的块（通常是2的幂次方），如果最后一个块不足，可以使用补零或填充的方式。
对每个数据块计算哈希值，得到叶节点。
如果叶节点的数量不是偶数，复制最后一个叶节点并加入到叶节点列表中，确保叶节点的数量是偶数。
迭代地将相邻的叶节点两两组合，计算它们的哈希值，得到父节点。如果有奇数个叶节点，可以将最后一个节点复制并参与哈希计算。
重复上述步骤，直到只剩下一个节点，即根节点。

**应用：**  
默克尔树的主要应用是在数字证书、区块链和文件系统中，用于快速验证数据的完整性。通过对每个数据块的哈希值进行逐级合并，可以有效地检测到数据的任何篡改或变化。
而且，默克尔树的节点可以被部分地验证，而不需要验证整个数据集，从而提高了效率。

运行结果：  
![image](https://github.com/yxh1120/Homework-group-41/blob/main/Project%2005/1.png)

实验环境：  
Visual studio 2020