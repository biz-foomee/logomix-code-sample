Markdown

# code-sample
データ解析コードサンプルです。

### 【ファイル構成】
* 解析用コード：`analysis_sample.Rmd`
* サンプルデータ①：`ph.csv`
* サンプルデータ②：`ab1.csv`
* サンプルデータ③：`ab2.csv`

### 【動かし方の注意点】
1. GitHubから各CSVファイルと `analysis_sample.Rmd` を取得
2. 以下のコピペ用データから、グラフ化したいサンプルのコードをコピー
3. `analysis_sample.Rmd` 先頭の `User settings` へペースト
4. Run  
※ブラウザからダウンロードして .txt になってしまった場合は .csv にリネームしてください。Download ZIPからのダウンロードの時はそのままでお使いください。

### 【コピペ用データ】
各ブロックを解析コードの先頭の "User settings" にコピー＆ペーストして実行してください。

####【サンプルデータ①：R1のpH検討】
```r
csv_name <- ph
item.lev <- c("505AEH", paste0("pH", c(6.954, 7.251, 7.471, 7.757, 8.135, 8.244, 8.540, 8.755, 8.956)))
a1cCal <- c(0, 5.9, 9.0, 13.2, 16.0)
```
####【サンプルデータ②：1次抗体量の検討】  
```r
csv_name <- ab1
item.lev <- paste0(seq(0.5, 1.5, by = 0.25), "% primAb")
a1cCal <- c(0, 5.9, 9.0, 13.2, 16.0)
```
####【サンプルデータ③：2次抗体量の検討】  
```r
csv_name <- ab2
item.lev <- paste0(seq(100, 130, by = 10), "% 2ndAb")
a1cCal <- c(0, 5.9, 9.0, 13.2, 16.0)
```
