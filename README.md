# CryptoCompare-data-capture
通过 cryptocompare.com 提供的API获取以小时为频率的数字货币历史交易数据
Get Crypto market history data with hour frequency through cryptocompare.com API

## 使用指南 Guide

共包含两个 jupyter notebook 文件：
Contains two jupyter notebook file:

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

## APIKey

APIkey可以通过注册 cryptocompare.com 免费得到

You can get a free APIkey after register cryptocompare.com

注意：中国大陆用户需要科学上网才可访问 cryptocompare.com

If you are not live in the Mainland China, there's no necessary to understand the above sentence :).

由于代码仍然处于测试调试阶段，并未对所有函数进行完整的封装，最终的运行主函数（尚未封装）均写在最后，可直接通过 Jupyter notebook 运行。

Not all functions are completely encapsulated, because the code is still in the testing and debugging stage. The main function (not encapsulated yet) is(are) written at the end of the code, and can be run directly through Jupyter notebook.

所需参数在代码中均提供了样例以及解释，如有任何疑问可通过邮件联系我

The required parameters are provided with examples and explanations in the code. If you have any questions, please contact me by email.

Email: jingyq233@gmail.com
