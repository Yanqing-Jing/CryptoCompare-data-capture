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

共包含两个 jupyter notebook 文件以及一个所有交易所列表的样例数据：

There are two jupyter notebook files and a sample dataset which contains all exchanges list:

### 1. get_crypto_exchanges: 

用于获取来自 cryptocompare.com 所记录的所有可用**交易所列表**，为帮助你自动获取所有交易对的历史交易数据。

Get all available exchanges list recorded in cryptocompare.com, which support you to get all history data of trading pairs automatically.

运行最后一段代码单元，即输出一份 .csv 文件，其中将会包含所有的**交易所**。

By running the last code cell, it would output a .csv file which records all exchanges.

### 2. cryptoCompare_data_capture_v2.0：

用于获取单个或者多个交易所下的交易对历史数据

Get multiple or specific history trading pairs of exchange(s).

运行最后两个代码块可分别获得单一交易对以及多个交易对的历史交易记录。

Run last two code cell to get the historical transaction records of a single trading pair or multiple trading pairs.

如果需要获取多个交易对的历史交易记录，请先运行 get_crypto_exchanges 以获得全部交易所列表，因为这是一个必须的参数。

If you want to get multiple historical transactions from many exchanges, please run 'get_crypto_exchanges' first to get all exchanges list wchich is a nessary parameter.

随后可以从获得的全部交易所列表中选择你想要的交易对，或者是全部的交易数据。
（警告：全部交易数据大致包含19930个交易对，总体大小约为60GB，全部获取预计需要80小时）

You can select pair(s) of exchange(s) data you whish to get from all exchanges list, or directly use the list to get all pairs
（Warning：All transactions pairs amount is about 19930, total size is about 60GB and estimate 60 hour to caupture）

### 3. all_ex.csv：

这个数据集是通过 'get_crypto_exchanges' 获取到的一个样例数据，包含了cryptocompare中提供的所有可用交易所下的所有交易对。

This dataset is from the result of 'get_crypto_exchanges', and contains all available pairs in all exchanges provided by cryptocompare.


## APIKey

APIkey可以通过注册 cryptocompare.com 免费得到

You can get a free APIkey after register cryptocompare.com

注意：中国大陆用户需要科学上网才可访问 cryptocompare.com

If you are not live in the Mainland China, there's no necessary to understand the above sentence :)


## 其他 Other info

由于代码仍然处于测试调试阶段，并未对所有函数进行完整的封装，最终的运行主函数（尚未封装）均写在最后，可直接通过 Jupyter notebook 运行。

Not all functions are completely encapsulated, because the code is still in the testing and debugging stage. The main function (not encapsulated yet) is(are) written at the end of the code, and can be run directly through Jupyter notebook.

所需参数在代码中均提供了样例以及解释，如有任何疑问可通过邮件联系我

The required parameters are provided with examples and explanations in the code. If you have any questions, please contact me by email.

Email: jingyq233@gmail.com

Reference：
https://min-api.cryptocompare.com/documentation
