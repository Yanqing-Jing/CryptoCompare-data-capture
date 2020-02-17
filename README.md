[toc]

# CryptoCompare-data-capture
通过 cryptocompare.com 提供的API获取以小时为频率的数字货币历史交易数据

Get Crypto market history data with hour frequency through cryptocompare.com API

## 使用指南 Guide

共包含两个 jupyter notebook 文件：

There are two jupyter notebook files:

### 1. get_crypto_exchanges: 

用于获取来自 cryptocompare.com 所记录的所有可用**交易所列表**，为帮助你自动获取所有交易对的历史交易数据。

Get all available exchanges list recorded in cryptocompare.com, which support you to get all history data of trading pairs automatically.

运行最后一段代码单元，即输出一份 .csv 文件，其中将会记录所有的**交易所**。

By running the last code cell, it would output a .csv file which records all exchanges.

### 2. cryptoCompare_data_capture_v2.0：

用于获取单个或者多个交易所下的交易对历史数据

Get multiple or specific history trading pairs of exchange(s).

运行最后两个代码块可分别获得单一交易对以及多个交易对的历史交易记录，将以 .csv 格式输出。

Run last two code cell to get the historical transaction records of a single trading pair or multiple trading pairs.

如果需要获取多个交易对的历史交易记录，请先运行 get_crypto_exchanges 以获得全部交易所列表，因为这是一个必须的参数。

If you want to get multiple historical transactions from many exchanges, please run 'get_crypto_exchanges' first to get all exchanges list wchich is a nessary parameter.

随后可以从获得的全部交易所列表中选择你想要的交易对，或者是全部的交易数据。
（警告：全部交易数据大致包含19930个交易对，总体大小约为60GB，全部获取预计需要80小时）

You can select pair(s) of exchange(s) data you whish to get from all exchanges list, or directly use the list to get all pairs
（Warning：All transactions pairs amount is about 19930, total size is about 60GB and estimate 60 hour to caupture）

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
