# logomix-code-sample
データ解析コードサンプルです。

【ファイル構成】

解析用コード：analysis_sample.Rmd

サンプルデータ①：260116 a1c505aeh r1ph r2_55 std.csv

サンプルデータ②：260310 a1c004afc 2ndconc std.csv 

サンプルデータ③：260310 a1c004afc primconc-1 std.csv

【動かし方の注意点】
① GitHubから上から各CSVファイルを取得
② 以下のcsvファイルごとのコピペ用データから、グラフ化したいサンプルのコードをコピー
② User settingsへコピペ用データをペースト
③ Run

【コピペ用データ】
各ブロックを解析コードの先頭の"User settings"にコピー＆ペーストして実行してください。

# サンプル1：R1 pH検討 
csv_name <- ph
item.lev <- c("505AEH", paste0("pH", c(6.954, 7.251, 7.471, 7.757, 8.135, 8.244, 8.540, 8.755, 8.956)))
a1cCal <- c(0, 5.9, 9.0, 13.2, 16.0)

# サンプル2：１次抗体濃度検討
csv_name <- ab1 
item.lev <- paste0(seq(0.5, 1.5, by = 0.25), "% primAb")
a1cCal <- c(0, 5.9, 9.0, 13.2, 16.0) 

# サンプル3：２次抗体濃度検討
csv_name <- ab2 
item.lev <- paste0(seq(100, 130, by = 10), "% 2ndAb")
a1cCal <- c(0, 5.9, 9.0, 13.2, 16.0) 
