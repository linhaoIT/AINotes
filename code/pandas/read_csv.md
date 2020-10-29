# pd.read_csv()
read csv as dataframe
## Usage
pd.read_csv(filepath_or_buffer, sep=',', delimiter=None, header='infer', names=None, index_col=None, usecols=None, squeeze=False, prefix=None, mangle_dupe_cols=True, dtype=None, engine=None, converters=None, true_values=None, false_values=None, skipinitialspace=False, skiprows=None, nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False, skip_blank_lines=True, parse_dates=False, infer_datetime_format=False, keep_date_col=False, date_parser=None, dayfirst=False, iterator=False, chunksize=None, compression='infer', thousands=None, decimal=b'.', lineterminator=None, quotechar='"', quoting=0, escapechar=None, comment=None, encoding=None, dialect=None, tupleize_cols=False, error_bad_lines=True, warn_bad_lines=True, skipfooter=0, skip_footer=0, doublequote=True, delim_whitespace=False, as_recarray=False, compact_ints=False, use_unsigned=False, low_memory=True, buffer_lines=None, memory_map=False, float_precision=None)

### Parameter
1. filepath_or_buffer:（这是唯一一个必须有的参数，其它都是按需求选用的）文件所在处的路径
2. sep：指定分隔符，默认为逗号','
3. delimiter : str, default None 定界符，备选分隔符（如果指定该参数，则sep参数失效）
4. header：int or list of ints, default ‘infer’ 指定哪一行作为表头。默认设置为0（即第一行作为表头），如果没有表头的话，要修改参数，设置header=None
5. names： 指定列的名称，用列表表示。一般我们没有表头，即header=None时，这个用来添加列名就很有用啦！
6. index_col: 指定哪一列数据作为行索引，可以是一列，也可以多列。多列的话，会看到一个分层索引
7. prefix: 给列名添加前缀。如prefix="x",会出来"x1"、"x2"、"x3"酱纸
8. nrows : int, default None 需要读取的行数（从文件头开始算起）
9. encoding: 乱码的时候用这个就是了，官网文档看看用哪个： https://docs.python.org/3/library/codecs.html#standard-encodings
10. skiprows : list-like or integer, default None 需要忽略的行数（从文件开始处算起），或需要跳过的行号列表（从0开始）。