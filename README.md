# Gale-ShapleyAlgorithm
Python版本    盖尔-沙普利算法:为了寻找一个稳定匹配而设计出的市场机制，对于市场的一方A有m个对象 另一方市场B有n个对象，A中的每个人会对B中的人有一个好感度排名，B也会有相应的排名 市场一方的对象 Ai，i=1,2,...,m 向另一方的对象 Bj，j=1,2,...,n 发出邀约，每个 Bj 会对接到的邀约进行比较，保留自己认为最好的，拒绝其它的。邀约被拒绝的 Ai 继续 向其它的 Bj 发出新的邀约，直到没有 Ai 希望再发出邀约为止。此时各 Bj 才最终接受 各自保留的邀约。该算法的一个关键之处在于，合意的邀约不会立即被接受，而只是暂时保 留不被拒绝，也就是 “延迟接受”。  注意：本算法不保证每个人都能找到相应的匹配，而是找到最稳定的匹配，即在双方这里 都没有办法找到更稳定的匹配，不会出现任一方可以接受更好的一人的可能性  算法思想： while  存在男人m是自由的且还没对每个女人都求过婚       选择这个男人m                 令w是m的优先表中还没求过婚的最高排名的女人         if  w是自由的  并且w愿意接受m             （m，w）变成约会状态         else  w当前与m1约会  并且w愿意接受m               if  w更偏爱m1而不爱m                     m保持自由               else    w更偏爱m而不爱m1                    （m，w）变成约会状态                     m1变成自由               endif                   endif endwhile  #本程序须知： #1.GS_matching的函数必须让list长度较小的一个在前面 #2.允许每个人可以接受的配对数不一样，即每个男士或者女士可以有数目不一样的青睐者 #3.允许男士和女士的数目不一样多 #4.返回的list里面若出现-1,则表明这个配对没有成功 可以在后续将这些进行剔除(已经进行了剔除，不会有没进行配对的出现在结果里面)  #输入和输出 输入是两个list集 具体的情况参照main方法里面的输入 输出是一个list  给出了具体的配对方式
