http://www.matrix67.com/blog/archives/4439
http://www.matrix67.com/blog/archives/497

第一次听说锈规作图问题是在2017megcup比赛中：https://2017.megcup.com/problems/4

你唯一可以做的操作是，以某个已知点为中心，以一个固定的长度为半径做圆，或者取已作的两圆的交点。这也就是传说中的“锈规作图”问题。

旷工们自然想到可以用细铁棍画圆，虽然很麻烦但至少有个长度单位。为了制造关键的正三角形木片，需要以任意给定的两点，用刚性细铁棍找到第三个点，使得三个点构成正三角形。现在他们将这个关键的任务交给了你！

输入格式
多组数据。每组三行，每行两个数，分别是第A、B、C点的坐标。

其中AC线段是细铁棍，即，你可以做的圆的半径。我们希望寻找D点，使得A、B、D构成等边三角形。

输出格式
每组多行。除了最后一行，每行格式是

    i# x y C a b
或
    i# x y P p
其中i是行号，从1开始编号。x、y是某个点的坐标。我们会以x、y为圆心，AC为半径自动帮你做一个圆，并将其命名为圆i。如果是是第一种格式，表示(x,y)是圆a和圆b的交点。如果是第二种格式，表示(x,y)是A、B、C之一。用p=1, 2, 3分别代表A、B和C点。

最后一行以D开头，格式为

    D x y C a b

表示找到的D点坐标为(x,y)，是圆a与圆b的交点。要求你做出的D点必须是某两个已做的圆的交点。

受精度限制，只有两个圆的圆心距超过1e-3才能求交点。

样例输入
0 0
2 0
0 2
0 0
1 0
0 1

样例输出
1# 0.0 0.0 P 1
2# 0.0 2.0 P 3
3# 2.0 0.0 P 2
D 1.0 1.73205080757 C 3 1
1# 0.0 0.0 P 1
2# 0.0 1.0 P 3
3# 1.0 0.0 P 2
D 0.5 0.866025403784 C 3 1