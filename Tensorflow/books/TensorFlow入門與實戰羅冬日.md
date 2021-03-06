>* TensorFlow入門與實戰 羅冬日
>* https://github.com/thewintersun/tensorflowbook

```
第1章　初識TensorFlow 1
1．1　TensorFlow特點 1
1．2　其他深度學習框架 3
1．2．1　Caffe 3
1．2．2　MXNet 3
1．2．3　Torch==> PyTorch
1．2．4　Theano 4
1．2．5　CNTK 5

第2章　TensorFlow環境搭建 6
2．1　安裝環境介紹 6
2．1．1　CUDA簡介 6
2．1．2　cuDNN簡介 6
2．1．3　查看機器的GPU資訊 7
2．2　安裝TensorFlow 8
2．2．1　安裝pip 9
2．2．2　通過pip安裝TensorFlow 9
2．2．3　源碼編譯安裝TensorFlow 10
2．3　NVIDIA驅動安裝 11
2．4　安裝CUDA和cuDNN 12
2．4．1　Linux下安裝CUDA 12
2．4．2　Linux下安裝cuDNN 13
2．4．3　Windows和Mac系統下安裝CUDA 14
2．4．4　Windows和Mac系統下安裝cuDNN 14
2．5　安裝測試 15

第3章　TensorFlow基礎 16
3．1　基本概念 16
3．1．1　張量 16
3．1．2　圖 17
3．1．3　操作 18
3．1．4　會話 19
```
```
#coding=utf-8
import tensorflow as tf

a = tf.Variable(1.0, name="a")
b = tf.add(a, 1, name="b")
c = tf.add(b, 1, name="c")
d = tf.add(b, 10, name="d")

summary_writer = tf.summary.FileWriter('./calc_graph' )
graph = tf.get_default_graph()
summary_writer.add_graph(graph)
summary_writer.flush()
```
```
3．2　變數 24
3．2．1　變數的初始化 24
3．2．2　變數的變形 25
3．2．3　資料類型和維度 26
3．2．4　共用變數和變數命名空間 27
3．3　模型的保存和載入 33
3．3．1　模型的保存 33
3．3．2　模型的載入 34
3．4　使用GPU 34
3．4．1　指定GPU設備 35
3．4．2　指定GPU顯存佔用 36
3．5　數據讀取 36
3．5．1　使用placeholder填充方式讀取資料 37
3．5．2　從檔讀入資料的方式 37
3．5．3　預先讀入記憶體的方式 48
3．6　利用TensorBoard進行資料視覺化 49
3．6．1　在TensorBoard中查看圖結構 49
3．6．2　訓練過程中單一資料變化趨勢 51
3．6．3　訓練過程中資料分佈視覺化 53
3．6．4　其他使用技巧 56

第4章　深度神經網路基礎 58
4．1　神經元 58
4．2　簡單神經網路 59
4．3　深度神經網路 62
4．4　損失函數 63
4．5　梯度下降 64
4．6　反向傳播 66
4．6．1　求導鏈式法則 66
4．6．2　反向傳播演算法思路 67
4．6．3　反向傳播演算法的計算過程 68
4．7　優化函數 72
4．7．1　隨機梯度下降優化演算法 72
4．7．2　基於衝量的優化演算法 73
4．7．3　Adagrad優化演算法 74
4．7．4　Adadelta優化演算法 75
4．7．5　Adam優化演算法 75
4．7．6　TensorFlow中的優化演算法API 76
4．8　一個簡單的例子 77

第5章　卷積神經網路 83
5．1　簡介 83
5．2　什麼是卷積 84
5．3　卷積神經網路基礎 88
5．3．1　局部感知野 88
5．3．2　參數共用 89
5．3．3　多卷積核 91
5．3．4　池化 92
5．3．5　多層卷積 93
5．4　卷積神經網路的訓練 94
5．4．1　池化層反向傳播 95
5．4．2　卷積層反向傳播 96
5．5　TensorFlow中的卷積神經網路 101
5．5．1　TensorFlow的卷積操作 101
5．5．2　TensorFlow的池化操作 103
5．6　用TensorFlow實現0和1數位識別 104
5．6．1　由圖片生成TFRecord檔 104
5．6．2　構建卷積網路結構 106
5．6．3　訓練過程 110
5．6．4　卷積過程資料的變化 114
5．7　幾種經典的卷積神經網路 117
5．7．1　AlexNet 117
5．7．2　VGGNet 118
5．7．3　Inception Net 120
5．7．4　ResNet 121

第6章　迴圈神經網路 123
6．1　普通RNN 123
6．1．1　普通RNN結構 123
6．1．2　普通RNN的不足 125
6．2　LSTM單元 126
6．2．1　LSTM單元基本結構 127
6．2．2　增加peephole的LSTM單元 131
6．2．3　GRU單元 132
6．3　TensorFlow中的RNN 132
6．4　用LSTM+CTC實現語音辨識 136
6．4．1　語音特徵介紹 136
6．4．2　計算流程描述 137
6．4．3　TensorFlow實現 139
6．5　在NLP中的應用 144
6．5．1　語言模型 144
6．5．2　詞向量 147
6．5．3　中文分詞 148


第7章　TensorFlow分散式 160
7．1　單機多GPU訓練 160
7．2　多機多GPU分散式訓練 163
7．2．1　參數伺服器 163
7．2．2　in-graph和between-graph模式 164
7．2．3　同步更新和非同步更新 165
7．2．4　非同步更新分散式示例 165
```
