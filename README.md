**InStock Stock System**

InStock stock system captures daily key data on stocks and ETFs, calculates various stock indicators, identifies various K-line forms, comprehensively selects stocks, has multiple built-in stock selection strategies, supports stock selection verification and backtesting, supports automatic trading, and supports Batch time, efficient operation, support for display on PCs, tablets, and mobile phones. It also provides Docker images for easy installation, making it a good helper for quantitative investment.

This project address: https://github.com/myhhub/stock

Docker image: https://hub.docker.com/r/mayanghua/instock **The image is optimized to build only 170M**.

# Function introduction

## 1: Comprehensive stock selection
Comprehensive stock selection supports more than 200 information columns in stock range, fundamentals, technical aspects, news, popularity indicators, market data, etc. for free combination stock selection. Stock selection conditions are divided into the following broad categories:
```
1. Stock range
Market, industry, region, concept, style, index components, time to market.
2. Fundamentals
Valuation indicators, per share indicators, profitability, growth ability, capital structure and solvency, equity shareholders.
3. Technical aspects
MACD golden cross, KDJ golden cross, heavy volume breakthrough, low capital net inflow, high net capital outflow, upward breakthrough of moving average, long moving average arrangement, short moving average arrangement, continuous rise and heavy volume, unlimited fall, one big positive line, two big positive lines, The rising sun rises in the east, is powerful in many directions, cannons stir up the clouds and see the sun, seven fairies descend to the earth (seven consecutive yins), eight immortals cross the sea (eight consecutive yangs), the nine-yang magical power (nine consecutive yangs), four strings of yang, the law of heaven, increase the volume to attack, and break the head and feet, Inverted Hammer, Shooting Star, Evening Star, Dawn, Pregnant, Dark Cloud Cover, Morning Star, Narrow Consolidation.
4. News surface
Announce major events, institutional attention, number of institutional shareholders, and institutional shareholding ratio.
5.Popularity indicator
Stock bar popularity rankings, changes in popularity rankings, consecutive rises in popularity rankings, consecutive declines in popularity rankings, new highs in popularity rankings, new lows in popularity rankings, proportion of new fans, proportion of die-hard fans, 7-day following rankings, and today's browsing rankings.
6. Market data
Stock price performance, transaction status, capital flow, market statistics, Shanghai and Shenzhen Stock Connect.
```
![](img/a3.jpg)
![](img/a2.jpg)
![](img/a1.jpg)

## 2: Daily stock data

Including daily stock data, stock capital flow, stock dividend distribution, stock dragon and tiger list, stock block transactions, stock fundamental data, industry capital flow, conceptual capital flow, and daily ETF data.

Capture the daily data of A stock, mainly some key data, and encapsulate the capture method to facilitate the expansion of the system to obtain data of personal concern.

![](img/00.jpg)
![](img/12.jpg)
## 3: Calculation of stock indicators
Calculate indicators based on talib and pandas, and the calculation is efficient and accurate. Adjust individual indicator formulas to ensure that the results are consistent with the results of Flush and Communication.
index:

```
1、MACD 2、KDJ 3、BOLL 4、TRIX，TRMA 5、CR 6、SMA 7、RSI 
8、VR，MAVR 9、ROC 10、DMI，+DI，-DI，DX，ADX，ADXR 11、W&R 
12、CCI 13、TR、ATR 14、DMA、AMA 15、OBV 16、SAR 17、PSY 
18、BRAR 19、EMV 20、BIAS 21、TEMA  22、MFI 23、VWMA
24、PPO 25、WT 26、Supertrend  27、DPO  28、VHF  29、RVI
30、FI 31、ENE 32、STOCHRSI
```

![](img/01.jpg)
![](img/06.jpg)
![](img/13.jpg)
![](img/10.jpg)
![](img/02.jpg)

## Four: Determine stocks to buy and sell

Determine stocks that may be bought or sold based on indicators. The specific screening conditions are as follows:


```
KDJ:
1. Overbought zone: When the K value is above 80, the D value is above 70, and the J value is above 90, it is overbought. Generally, stock prices are likely to fall. Investors should be cautious, outsiders should not chase the rise, and insiders should sell when appropriate.
2. Oversold zone: The K value is below 20, and the D value is below 30. This is the oversold zone. Generally speaking, the stock price is likely to rise, and the possibility of rebound increases. Insiders should not sell stocks easily, while outsiders can look for opportunities to enter.
RSI:
1. When the six-day indicator rises to 80, it means that the stock market is overbought. If it continues to rise and exceeds 90, it means that it has reached the warning zone of serious overbought, and the stock price has formed a head, and it is very likely to rise in the short term. Internal reversal.
2. When the six-day strength indicator drops to 20, it means that the stock market is oversold. If it continues to drop below 10, it means that it has reached the severely oversold area, and the stock price is likely to have the opportunity to stop falling and rebound.
CCI:
1. When CCI＞﹢100, it indicates that the stock price has entered the abnormal range - the overbought range, and you should pay more attention to the abnormal movement of the stock price.
2. When CCI <﹣100, it indicates that the stock price has entered another abnormal range - the oversold range, and investors can buy stocks at low prices.
CR:
1. When it falls below the four lines a, b, c, and d, and then climbs up 160 from the low point, it is a good opportunity for short-term profits, and the stock should be sold appropriately.
2. When CR falls below 40, it is a good opportunity to open a position.
WR:
1. When the %R line reaches 20, the market is in an overbought condition and the trend may be about to peak.
2. When the %R line reaches 80, the market is in an oversold condition and the stock price trend may bottom out at any time.
VR:
1. The profit area is 160-450 and profit is taken according to the situation.
2. You can buy in the low price area of ​​40-70.
```

![](img/05.jpg)

## Five: K-line pattern recognition

Accurately identify 61 K-line forms and support user-selected form recognition.

Recognition form:

```
1. Two Crows 2. Three Crows 3. Three Internal Rise and Fall 4. Three Line Strikes 5. Three External Rise and Fall 6. Southern Three Stars 7. Three White Soldiers 8. Abandoned Baby
9. The enemy is now 10. Belt-catching line 11. Breakaway 12. Closing missing shadow line 13. Hidden baby engulfed 14. Counterattack line 15. Dark cloud top 16. Cross 17. Cross star
18. Dragonfly Cross/T-Shaped Cross 19. Devouring Pattern 20. Cross Evening Star 21. Evening Star 22. Up/Down Gap and Parallel Yang Line 23. Tombstone Cross/Inverted T Cross
24. Hammer 25, hanging man 26, mother-child line 27, cross harami 28, high wind and waves line 29, trap 30, correction trap 31, domestic pigeon 32, triplet crow
33. Inner neck line 34. Inverted hammer 35. Rebound pattern 36. Rebound pattern determined by long missing shadow line 37. Ladder bottom 38. Long leg cross 39. Long candle
40. Bald head and bare feet/missing shadow line 41. Same low price 42, foreshadowing 43, cross morning star 44, morning star 45, upper neck line 46, piercing pattern 47, rickshaw driver
48. Three rising/falling methods 49. Separation line 50. Shooting star 51. Short candle 52. Spindle 53. Pause pattern 54. Bar sandwich 55. Water detection rod
56. Gap and parallel Yin and Yang lines 57. Insertion 58. Three stars 59. Strange three river beds 60. Two crows jumping upward 61. Three methods of ascending/descending gaps
```
Shape recognition results:
```
Negative: A sell signal occurs
0: This form does not appear
Positive: A buy signal appears
```
![](img/09.jpg)

![](img/06.jpg)

## Six: Strategic stock selection

It has built-in multiple stock selection strategies such as heavy volume rising, landing pad, retracing the annual line, breaking through the platform, heavy volume falling limit, etc., and also encapsulates the strategy template to facilitate expansion and implementation of your own strategies.


```
1. Increase in volume
 1) The current day's increase is less than 2% compared with the previous day or the closing price is less than the opening price.
 2) The transaction volume on the day shall not be less than 200 million.
 3) Today’s trading volume/5-day average trading volume >=2.
2. Long moving average
 MA30 up
 1) The 30-day moving average 30 days ago < the 30-day moving average 20 days ago < the 30-day moving average 10 days ago < the 30-day moving average of the current day.
 2) (30-day moving average of the current day/30-day moving average 30 days ago)>1.2.
3. Helipad
 1) There has been an increase of more than 9.5% in the last 15 days, and it must be a large-volume increase.
 2) The next trading day must open higher, the closing price must rise, and the difference from the opening price cannot be greater than or equal to 3%.
 3) The next 2 or 3 trading days must open higher, the closing price must rise, and the difference from the opening price cannot be greater than or equal to 3%, and the daily increase or decrease must be within 5%.
4. Return to the New Year line
 1) Divided into 2 time periods: the previous period = the trading day before the highest closing price in the last 60 trading days (length > 0), and the latter period = the highest price day and the following trading days.
 2) In the previous period, it broke upward from below the annual line (250 days).
 3) The later period must run above the annual line, and the difference between the lowest price day and the highest price day in the latter period must be between 10 and 50 days.
 4) The retracement is accompanied by shrinkage: the highest price daily trading volume/the lowest price daily trading volume in the later period>2, and the lowest price/highest price in the later period<0.8.
5. Breakthrough platform
 1) The closing price of a certain day within 60 days >= 60-day moving average > opening price.
 2) And [1] increases in volume.
 3) And before [1], the closing price of any day deviated from the 60-day moving average by between -5% and 20%.
6. No significant retracement
 1) The increase in the closing price on the day compared with the closing price 60 days ago is less than 0.6.
 2) In the past 60 days, there cannot be a single-day decline of more than 7%, a high opening and low moving of 7%, a two-day cumulative decline of 10%, and a two-day high opening and low moving of 10%.
7. Turtle Trading Rules
 The closing price on the last trading day is the highest price within the specified range.
 1) The closing price of the day >= the highest closing price in the last 60 days.
8. Tall and narrow flag shape
 1) Must be listed and traded for at least 60 days.
 2) The closing price of the day/the lowest price of the previous 24 to 10 days >= 1.9.
 3) The increase must be greater than or equal to 9.5% for two consecutive days in the previous 24 to 10 days.
9. Increase the volume and lower the limit.
 1) Down >9.5%.
 2) The transaction volume is not less than 200 million.
 3) The trading volume is at least 4 times the 5-day average trading volume.
10. Low ATR growth
 1) Must be listed and traded for at least 250 days.
 2) The highest closing price in the last 10 trading days must be 1.1 times higher than the lowest closing price in the last 10 trading days.
11. Stock selection based on stock fundamentals
 1) The P/E ratio is less than or equal to 20 and greater than 0.
 2) The price-to-book ratio is less than or equal to 10.
 3) The return on net assets is greater than or equal to 15.## Six: Strategic stock selection

It has built-in multiple stock selection strategies such as heavy volume rising, landing pad, retracing the annual line, breaking through the platform, heavy volume falling limit, etc., and also encapsulates the strategy template to facilitate expansion and implementation of your own strategies.


```
1. Increase in volume
 1) The current day's increase is less than 2% compared with the previous day or the closing price is less than the opening price.
 2) The transaction volume on the day shall not be less than 200 million.
 3) Today’s trading volume/5-day average trading volume >=2.
2. Long moving average
 MA30 up
 1) The 30-day moving average 30 days ago < the 30-day moving average 20 days ago < the 30-day moving average 10 days ago < the 30-day moving average of the current day.
 2) (30-day moving average of the current day/30-day moving average 30 days ago)>1.2.
3. Helipad
 1) There has been an increase of more than 9.5% in the last 15 days, and it must be a large-volume increase.
 2) The next trading day must open higher, the closing price must rise, and the difference from the opening price cannot be greater than or equal to 3%.
 3) The next 2 or 3 trading days must open higher, the closing price must rise, and the difference from the opening price cannot be greater than or equal to 3%, and the daily increase or decrease must be within 5%.
4. Return to the New Year line
 1) Divided into 2 time periods: the previous period = the trading day before the highest closing price in the last 60 trading days (length > 0), and the latter period = the highest price day and the following trading days.
 2) In the previous period, it broke upward from below the annual line (250 days).
 3) The later period must run above the annual line, and the difference between the lowest price day and the highest price day in the latter period must be between 10 and 50 days.
 4) The retracement is accompanied by shrinkage: the highest price daily trading volume/the lowest price daily trading volume in the later period>2, and the lowest price/highest price in the later period<0.8.
5. Breakthrough platform
 1) The closing price of a certain day within 60 days >= 60-day moving average > opening price.
 2) And [1] increases in volume.
 3) And before [1], the closing price of any day deviated from the 60-day moving average by between -5% and 20%.
6. No significant retracement
 1) The increase in the closing price on the day compared with the closing price 60 days ago is less than 0.6.
 2) In the past 60 days, there cannot be a single-day decline of more than 7%, a high opening and low moving of 7%, a two-day cumulative decline of 10%, and a two-day high opening and low moving of 10%.
7. Turtle Trading Rules
 The closing price on the last trading day is the highest price within the specified range.
 1) The closing price of the day >= the highest closing price in the last 60 days.
8. Tall and narrow flag shape
 1) Must be listed and traded for at least 60 days.
 2) The closing price of the day/the lowest price of the previous 24 to 10 days >= 1.9.
 3) The increase must be greater than or equal to 9.5% for two consecutive days in the previous 24 to 10 days.
9. Increase the volume and lower the limit.
 1) Down >9.5%.
 2) The transaction volume is not less than 200 million.
 3) The trading volume is at least 4 times the 5-day average trading volume.
10. Low ATR growth
 1) Must be listed and traded for at least 250 days.
 2) The highest closing price in the last 10 trading days must be 1.1 times higher than the lowest closing price in the last 10 trading days.
11. Stock selection based on stock fundamentals
 1) The P/E ratio is less than or equal to 20 and greater than 0.
 2) The price-to-book ratio is less than or equal to 10.
 3) The return on net assets is greater than or equal to 15.
```

![](img/04.jpg)

## Seven: Stock selection verification


Backtest the stocks selected by indicators, strategies, etc. to verify the success rate of the strategy and whether it is available.


![](img/05.jpg)

## Eight: Automatic trading

It supports automatic trading, with built-in strategies and example strategies for automatically buying new stocks. Since money is involved, there may be risks involved, and no other trading strategies are provided.

Has a trading log and supports configuring a trading log for each trading strategy.

**Special reminder**: A new transaction will be triggered at 10:00 on the trading day. If you do not want to create a new transaction, delete stagging.py or do not start the "Trading Service".

![](img/11.jpg)

## Nine: Pay attention to the function

Supports stock following, and the following stocks will be displayed at the top and highlighted in red in each module (included).

## Ten: Support batch


You can perform indicator calculation, strategic stock selection, backtesting, etc. through time period, enumeration time, and current time. It also supports intelligent identification of transaction days, and any date can be entered.

The specific execution settings are as follows:
```
------Overall operation, support batch operation------
Current time job python execute_daily_job.py
Single time job python execute_daily_job.py 2022-03-01
Enumerate time jobs python execute_daily_job.py 2022-01-01, 2021-02-08, 2022-03-12
Interval time job python execute_daily_job.py 2022-01-01 2022-03-01

------Single-function job, supports batch job, backtest data is automatically filled to the current
Basic data real-time job python basic_data_daily_job.py
Basic data non-real-time job python basic_data_other_daily_job.py
Indicator data job python indicators_data_daily_job.py
K-line pattern job klinepattern_data_daily_job.py
Strategy data job python strategy_data_daily_job.py
Backtest data python backtest_data_daily_job.py
```

## 11: Storage adopts database design

Data storage adopts database design, which can save historical data and perform extended analysis, statistics and mining of data. The system automatically creates databases and data tables, and encapsulates batch updates and data insertions to facilitate business expansion.

![](img/07.jpg)

## 12: Display using web design

Use web design to visually display the results. Encapsulate the display, add new business forms, and only need to configure the view dictionary to automatically display the business visualization interface to facilitate the expansion of business functions.

## Thirteen: Efficient operation


Multi-threading and single-case shared resources are used to effectively improve computing efficiency. All tasks such as capturing one day's data, calculating indicators, pattern recognition, strategic stock selection, and backtesting take about 4 minutes to run (an ordinary notebook). The more days of calculation, the higher the efficiency.


## Fourteen: Convenient debugging

Important logs of system operation are recorded in stock_execute_job.log (data capture, processing, analysis), stock_web.log (web service), stock_trade.log (trading service) to facilitate debugging and problem discovery.

![](img/08.jpg)


# Installation instructions

This system supports Windows, Linux, and MacOS. At the same time, this system has created a Docker image and you can choose the installation method according to your needs.

The following will explain one by one according to the conventional installation method and the docker image installation method.

## 1: Conventional installation method

It is recommended to install under Windows, which is convenient to operate and use the system, and the installation is also very simple.

The following installation and operation are introduced using Windows as an example.

### 1. Install python

The project is developed using python 3.11, the latest version is recommended.

```
(1) Download the installation package from the official website https://www.python.org/downloads/ and install it with one click. Remember to check Automatically set environment variables during installation.
(2) Configure a permanent global domestic image library (because of the wall, the library files cannot be installed normally) and execute the following dos command:
python pip config --global set global.index-url https://mirrors.aliyun.com/pypi/simple/
# If you only want to set it for the current user, you can also remove the "--global" option below
```
### 2. Install mysql

The latest version is recommended.

```
Download the installation package from the official website https://dev.mysql.com/downloads/mysql/ and install it with one click.
```
### 3. Install dependent libraries

The dependent libraries are all the latest versions.

a. Install dependent libraries:

```
#dosSwitch to the root directory of this system and execute the following command:
python pip install -r requirements.txt
```
b. If you want to upgrade the project's dependent library to the latest version, you can use the following method:

First open requirements.txt, then modify "==" in the file to ">=", and then execute the following command:

```
python pip install -r requirements.txt --upgrade
```

c. If you extend this project, you can generate project dependencies through the following method:

```
#Use pipreqs to generate requirements.txt for project-related dependencies

python pip install pipreqs
#Install pipreqs, skip it if installed

python pipreqs --encoding utf-8 --force ./
# This project is utf-8 encoding
```

### 4. Install talib

```
The first method. Install under pip
(1) Download and decompress ta-lib-0.4.0-msvc.zip from https://www.ta-lib.org/
(2) Unzip and place ta_lib in the root directory of drive C
(3) Download and install Visual Studio Community from https://visualstudio.microsoft.com/zh-hans/downloads/. Remember to check the Visual C++ function during installation.
(4)Build TA-Lib Library #Build TA-Lib library
 ① Search and open [Native Tools Command Prompt] in the start menu (select 32-bit or 64-bit according to the operating system)
 ②Enter cd C:\ta-lib\c\make\cdr\win32\msvc
 ③Build the library and enter nmake
(5) The installation is completed.
The second method. Install under Anaconda
(1) Open the Anaconda Prompt terminal.
(2) Enter the command line conda install -c conda-forge ta-lib in the terminal.
(3) Confirm here whether to continue the installation? Enter y to continue the installation until it is complete
(4) The installation is completed.
```
### 5. Install Navicat (optional)

Navicat can easily manage databases and manually view, process, analyze, and mine data.

Navicat is a set of database management tools that can create multiple connections to facilitate the management of different types of databases such as MySQL, Oracle, PostgreSQL, SQLite, SQL Server, MariaDB and MongoDB.

```
(1) Download the installation package from the official website https://www.navicat.com.cn/download/navicat-premium and install it with one click.

(2) Then download the crack patch: https://pan.baidu.com/s/18XpTHrm9OiLEl3u6z_uxnw Extraction code: 8888, just crack it.
```
### 6. Configure database

Generally, the information that may be modified is the "database access password".

Modify database.py related information:

```
db_host = "localhost" # Database service host
db_user = "root" # Database access user
db_password = "root" # Database access password
db_port = 3306 # Database service port
db_charset = "utf8mb4" # Database character set
```

### 7. Install automated trading (optional)

```
1. Install trading software
 1.1 Customers of General Flush Client Brokerage
 Universal Flush Client:
 https://activity.ths123.com/acmake/cache/1361.html
 1.2 Customers of dedicated Flush client brokers
 Go to the official website of the brokerage company to find the special version of Flush.
 For example: Guangfa’s downloadable new independent client (flush version):
 http://www.gf.com.cn/softdownload/index?tab=1
2. Install tesseract (automatically recognize verification code)
 The first method. Download the compiled
 On the link below, select the appropriate version based on your operating system.
 https://digi.bib.uni-mannheim.de/tesseract/
 The second method. Compile with source code
 Download source code: https://github.com/tesseract-ocr/tesseract
 Notice:
 After installation, set the installation path to the PATH environment variable.
 The dos command settings are provided below. Run cmd as administrator and enter:
 setx /m PATH "%PATH%;C:\Program Files\Tesseract-OCR"
3.Set transaction configuration
 3.1. Modify trade_client.json
 "user": "888888888888", #Trading account
 "password": "888888", #Transaction password
 "exe_path": "C:/gfzqrzrq/xiadan.exe" #Trading software path
 3.2. Modify trade_service.py
 broker = 'gf_client' #This is Guangfa
 For details, please refer to usage.md and configure the corresponding brokerage firm.
```

### 8. Operation instructions

#### 8.1. Perform data capture, processing, analysis, and identification

Batch jobs are supported, please refer to the comments in run_job.bat for details.

It is recommended to add it to the task plan and execute it at 17:00 every day on working days.

**Data capture and processing principles:**

1). Available at the opening of the market and without historical data: comprehensive stock selection, daily stock data, stock capital flow, stock dividend distribution, dragon and tiger list, daily ETF data;

2). Available at the closing price and with historical data: stock indicator data, stock K-line patterns, and stock strategy data;

3). Historical data is only available 1 to 2 hours after the market closes: block trades.

Running run_job.bat will obtain the current or previous trading day data of each module according to the above principles.

```

Run run_job.bat
```
If you want to see the current real-time data after the market opens, you can run the following, which will take about 1 second:

```
#Basic data job
python basic_data_daily_job.py
```
#### 8.2. Start web service

```
Run run_web.bat
```
After starting the service, open the browser and enter: http://localhost:9988/ to use the visualization function of this system.

#### 8.3. Start trading service

```
Run run_trade.bat
```

## 2: Docker image installation method

If there is no docker environment, you can refer to: [VirtualBox virtual machine installation Ubuntu](https://www.ljjyy.com/archives/2019/10/100590.html), which also introduces the installation of common software such as python and docker. If I want to install docker on Baidu myself under Windows.

### 1. Install database mirroring

If you already have Mysql or MariaDB database, you can skip this step.

Run the following command:

**Special reminder: The user executing the command must have root privileges, and the same applies to other commands. For example: In ubuntu system, add sudo** and sudo docker before the command.
