# pd.to_csv()
Write to csv
## Usage
to_csv(path_or_buf, sep, na_rep, columns, header, index)
## Parameter
1. path_or_buf：字符串，放文件名、相对路径、文件流等；
2. sep：字符串，分隔符，跟read_csv()的一个意思
3. na_rep：字符串，将NaN转换为特定值
4. columns：列表，指定哪些列写进去
5. header：默认header=0，如果没有表头，设置header=None，表示我没有表头呀！
6. index：关于索引的，默认True,写入索引