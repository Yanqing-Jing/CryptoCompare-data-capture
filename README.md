# CryptoCompare-data-capture
通过 cryptocompare.com 提供的API获取以小时为频率的数字货币历史交易数据

Get Crypto market history data with hour frequency through cryptocompare.com API

## 2020.03.13 更新
提交 cryptoCompare_data_capture_v3.0 版本，对过去版本进行了优化以及功能升级
1. 对服务器端限制进行了优化升级，提升了批量数据的获取效率
2. 新增了数据获取时间预估以及时间统计，增加使用体验
3. 优化了同一交易对数据多次获取的数据拼接时的bug
4. 新增了历史数据保存功能，会自动将上次产生的数据进行归档保存，并存储每次获取数据的执行时间戳
5. 优化了终端显示信息，增加使用体验
6. 新增了一个交易对列表，缩减了大部分小众交易对，仅保留了热门交易对和交易所（强烈推荐使用此交易列表作为数据抓取参考）

Commit version cryptoCompare_data_capture_v3.0, improved function and effectiveness
1. Fixed the data accessing limitation from cryptoCompare, improved effectiveness of bulk data capturing
2. Added time consuming and time statistic of capturing improved user experience
3. Fixed the error when appending multiple data file
4. Added history file storage function, and automatically store last time data capture file as well as the timestamp
5. Improved terminal info display and user experience
6. Added a new exchange and pair address book, reduced minority pairs and remained popular pairs(Highly recommend to use this address book as the data capturing reference)



## 使用指南 Guide

共包含两个主要的 jupyter notebook 文件以及2个所有交易所列表的样例数据：

There are two mainly jupyter notebook files and 2 sample datasets which contains all exchanges list:

### 1. get_crypto_exchanges: 

用于获取来自 cryptocompare.com 所记录的所有可用**交易所列表**，为帮助你自动获取所有交易对的历史交易数据。

Get all available exchanges list recorded in cryptocompare.com, which support you to get all history data of trading pairs automatically.

运行最后一段代码单元，即输出一份 .csv 文件，其中将会包含所有的**交易所**。

By running the last code cell, it would output a .csv file which records all exchanges.

### 2. cryptoCompare_data_capture_v2.0/v3.0：

用于获取单个或者多个交易所下的交易对历史数据

Get multiple or specific history trading pairs of exchange(s).

运行最后两个代码块可分别获得单一交易对以及多个交易对的历史交易记录。

Run last two code cell to get the historical transaction records of a single trading pair or multiple trading pairs.

如果需要获取多个交易对的历史交易记录，请使用提供的样例交易对数据（all_ex.csv 或者 ex_filter.csv），或运行 get_crypto_exchanges 以获得全部交易所列表。这是一个必须的参数。

If you want to get multiple historical transactions from many exchanges, please use sample exchanges and pairs address book(all_ex.csv or ex_filter.csv) , or run 'get_crypto_exchanges' first to get all exchanges list. It is a nessary parameter.

（警告：全部交易数据大致包含19930个交易对，总体大小约为60GB，全部获取预计需要80小时,建议使用部分交易对 ex_filter.csv）

（Warning：All transactions pairs amount is about 19930, total size is about 60GB and estimate 60 hour to caupture, recommend to use partial pairs from ex_filter.csv）

### 3. all_ex.csv / ex_filter.csv：

all_ex.csv 数据集是通过 'get_crypto_exchanges' 获取到的一个样例数据，包含了cryptocompare中提供的所有可用交易所下的所有交易对。

all_ex.csv dataset is from the result of 'get_crypto_exchanges', and contains all available pairs in all exchanges provided by cryptocompare.

ex_filter.csv 数据集是经过综合排名筛选出的部分热门交易所和交易对

ex_filter.csv dataset is popular exchanges and pairs filtered by comprehensive ranking 

## APIKey

APIkey可以通过注册 cryptocompare.com 免费得到

You can get a free APIkey after register cryptocompare.com

注意：中国大陆用户需要科学上网才可访问 cryptocompare.com

If you are not live in the Mainland China, there's no necessary to understand the above sentence :)

## 常见问题 Common errors

1. all_ex.csv or ex_filter.csv not found

请把上述两个文件放置于C:/User/yourUserName目录下
Place those two file at location C:/User/yourUserName

2. 服务器访问被无限阻止 Connection infinite refused by the server.
   a. 检查网络连接状态
   b. 中国大陆境内需翻墙
   c. 检查以下三个文件夹/文件是否被正常创建:
    'D:/Data'
    'D:/Data_history_time/data_history.txt'
    'D:/Data_history'
    
    a. Check your internet connectivity
    b. Need a VPN if you are staying in mainland china
    c. Check if the following three folders / files are created correctly:
     'D:/Data'
     'D:/Data_history_time/data_history.txt'
     'D:/Data_history'

## 其他 Other info

由于代码仍然处于测试调试阶段，并未对所有函数进行完整的封装，最终的运行主函数（尚未封装）均写在最后，可直接通过 Jupyter notebook 运行。

Not all functions are completely encapsulated, because the code is still in the testing and debugging stage. The main function (not encapsulated yet) is(are) written at the end of the code, and can be run directly through Jupyter notebook.

所需参数在代码中均提供了样例以及解释，如有任何疑问可通过邮件联系我

The required parameters are provided with examples and explanations in the code. If you have any questions, please contact me by email.

Email: jingyq233@gmail.com

Reference：
https://min-api.cryptocompare.com/documentation
