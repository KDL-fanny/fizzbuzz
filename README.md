## プログラムの概要
このプログラムは、指定された最大値までの FizzBuzz を表示します。数字が 3 で割り切れる場合は "Fizz"、5 で割り切れる場合は "Buzz"、3 と 5 両方で割り切れる場合は "FizzBuzz" を表示します。それ以外の場合はその数字をそのまま表示します。

このプログラムは Python で実装されており、Docker コンテナ内で実行することができます。

## ビルド方法
1. 必要なファイルが揃っていることを確認してください（`test1.py`, `Dockerfile`）。
2. 以下のコマンドで Docker イメージをビルドします。

```bash
docker build -t my-fizzbuzz-image .
```
このコマンドで my-fizzbuzz-image という名前の Docker イメージが作成されます。

## 実行方法
ビルドが完了したら、以下のコマンドでコンテナを実行します。引数として最大値を指定してください。
（例：100）
```bash
docker run --name my-fizzbuzz-container my-fizzbuzz-image 100
```
最大値として 100 を指定して、1 から 100 までの FizzBuzz 結果が表示されます。

## 実行例（実際の出力結果を含む）
最大値として 100 を指定すると、以下のように出力されます
```bash
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
Buzz
Fizz
22
23
Fizz
Buzz
26
Fizz
28
29
FizzBuzz
31
32
Fizz
34
Buzz
Fizz
37
38
Fizz
Buzz
41
Fizz
43
44
FizzBuzz
46
47
Fizz
49
Buzz
Fizz
52
53
Fizz
Buzz
56
Fizz
58
59
FizzBuzz
61
62
Fizz
64
Buzz
Fizz
67
68
Fizz
Buzz
71
Fizz
73
74
FizzBuzz
76
77
Fizz
79
Buzz
Fizz
82
83
Fizz
Buzz
86
Fizz
88
89
FizzBuzz
91
92
Fizz
94
Buzz
Fizz
97
98
Fizz
Buzz
```

＊実際の実行結果
<img width="1129" alt="スクリーンショット 2025-06-18 11 52 00" src="https://github.com/user-attachments/assets/ffbb1b43-2d0b-469b-8dde-b796763f2694" />
<img width="1118" alt="スクリーンショット 2025-06-18 11 52 25" src="https://github.com/user-attachments/assets/fd715139-1461-44e3-8940-b2b2bc5ed9b3" />

## その他情報
1. 既存のコンテナを停止の場合
   まず、現在の my-fizzbuzz-container を停止します。
```bash
docker stop my-fizzbuzz-container
```

2. 既存のコンテナを削除の場合
   その後、停止したコンテナを削除します。
```bash
docker rm my-fizzbuzz-container
```

3. 新しいコンテナを実行
   既存のコンテナを削除した後、新しいコンテナを実行します。
```bash
docker run --name my-fizzbuzz-container my-fizzbuzz-image 100
```
