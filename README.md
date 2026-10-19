# backtest_python

FMZ backtest engine python package
support python2 and python3, support Windows, Linux, Mac

## install

```
pip install https://github.com/fmzquant/backtest_python/archive/master.zip
```

OR

```
pip3 install https://github.com/fmzquant/backtest_python/archive/master.zip
```

## simple example
```python
'''backtest
start: 2022-02-19 00:00:00
end: 2022-03-22 12:00:00
period: 15m
exchanges: [{"eid":"Binance","currency":"BTC_USDT","balance":10000,"stocks":0}]
'''
from fmz import *
task = VCtx(__doc__) # initialize backtest engine from __doc__
print(exchange.GetAccount())
print(exchange.GetTicker())
print(task.Join(True)) # print backtest result
task.Show() # or show backtest chart
```

The config string can be generated automatically by saving the backtest configuration in the strategy edit page.

配置字符串可以通过策略编辑界面里的保存回测配置来自动生成

![meta](https://www.fmz.com/upload/asset/aa67494fc6306759753385bf7634ee4cd437f3f2.png) 
 
## api
https://www.fmz.com/api



MIT License

Copyright (c) 2026 @Lakr233

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
