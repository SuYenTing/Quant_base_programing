---
title: "Tidyquant�M�󤶲�"
author:
  - "���ɱб�: ���s�j�ǰ]�Ⱥ޲z�Ǩt ���L�� �б�"
  - "�峹���g: ���s�j�ǰ]�Ⱥ޲z�Ǩt Ĭ�ۮx ��s�U�z"
date: "2018�~6��7��"
output: 
  html_document:
    keep_md: true
css: css_config.css
---



--------------------------------------------------

## �e��

R�y���b�]�Ȼ�줤�A�`�Ψ쪺�M��j�����U�C�X�ӡG

* [xts](https://cran.r-project.org/web/packages/xts/xts.pdf)/[zoo](https://cran.r-project.org/web/packages/zoo/zoo.pdf): �B�z�ɶ��ǦC���M��C
* [TTR](https://cran.r-project.org/web/packages/TTR/TTR.pdf): �p����ĸ겣�޳N���Ф��M��C
* [quantmod](https://cran.r-project.org/web/packages/quantmod/quantmod.pdf): ���ĸ겣�޳N���R�^���M��A�i��[Yahoo Finance](https://finance.yahoo.com/)��[Google Finance](https://finance.google.com/)�U�����v�ѻ��ƾکΨ�L���Ĭ����ƾڡC�åB��X`TTR`�M��Aø�s�X�}�G���޳N���R�ϪR�C
* [PerformanceAnalytics](https://cran.r-project.org/web/packages/PerformanceAnalytics/PerformanceAnalytics.pdf): �p����ĸ겣���S�Z�ī��Ф��M��C

�{�b��R�y���b��Ƭ�Ǫ����餧�U�A��Ƽƾڮ榡�w���V[tidy data](https://cran.r-project.org/web/packages/tidyr/vignettes/tidy-data.html)�Φ��C[tidyverse](https://www.tidyverse.org/)�M��w�O�C��R�ϥΪ̥��Ǫ��M��A�ϥΦ��M������ƾ�z���{���X²��S�ֳt�A��R�y������K���ڦV�󰪤@�h�C�M�Ӧb�]�Ȼ�쪺�M��A�ثe�ҬO�H�ɶ��ǦC��Ʈ榡(xts)����¦�غc�Ӧ��C�N�Y�n�ϥγo�ǮM�󪺨�ƮɡA�ݭn���N��ƥ��ରxts�榡�A�~�వ�]�Ȥ��R�C�Y�n�b`tidyverse`�M�󤤨ϥγo�ǰ]�Ȼ��M�󪺨�ơA�|���\�h����A�ݭn���B�~����z�~��ϥΡA�D�`����K�C

�w��o�ӵh�I�AR�y�����H���X�ӸѨM�o�Ӱ��D�AMatt Dancho�MDavis Vaughan�}�o�X[tidyquant](https://cran.r-project.org/web/packages/tidyquant/tidyquant.pdf)�M��A���]�Ȼ��M��P`tidyverse`�M��f�_�@�y����A��`tidyverse`�M�����ܻ����a�ϥΰ]�Ȼ��M��C

<img src="tidyquant�ܷN��.png" width="600px" height="400px" style="display: block; margin: auto;" />
<center>��1 tidyquant�M��ܷN��</center>
<center>(�Ϥ��I�ܩ�tidyquant�M��[�v������](https://www.youtube.com/embed/woxJZTL2hok))</center>

`tidyquant`�M�󪺧@��Matt Dancho�g�X�\�h�Ժɪ������d���ɮסA�i�ѦҥH�U�s��:

* [Introduction to tidyquant](https://cran.r-project.org/web/packages/tidyquant/vignettes/TQ00-introduction-to-tidyquant.html)
* [Core Functions in tidyquant](https://cran.r-project.org/web/packages/tidyquant/vignettes/TQ01-core-functions-in-tidyquant.html#get-quantitative-data)
* [R Quantitative Analysis Package Integrations in tidyquant](https://cran.r-project.org/web/packages/tidyquant/vignettes/TQ02-quant-integrations-in-tidyquant.html)
* [Scaling and Modeling with tidyquant](https://cran.r-project.org/web/packages/tidyquant/vignettes/TQ03-scaling-and-modeling-with-tidyquant.html)
* [Charting with tidyquant](https://cran.r-project.org/web/packages/tidyquant/vignettes/TQ04-charting-with-tidyquant.html)
* [Performance Analysis with tidyquant](https://cran.r-project.org/web/packages/tidyquant/vignettes/TQ05-performance-analysis-with-tidyquant.html)

��M�A���g�峹�������]���O�q�H�W�������d���ɮרӾǲߨüg�X�Ӫ��I�t�O�b��ڭ̬O�Τ��廡���λO�W���ѥ������ƨӰ��d�ҡA�åu�^�����n�����A���j�a�i�H�ֳt�a�x���ߵ��C

--------------------------------------------------

## �ƾڤU��

���ѥ����R���Ĥ@�B�N�O�n���o�ѻ���ơA`tidyquant`�M��`tq_get()`��ƾ�X`quantmod`�M��`getSymbols()`��ơC�z�L`tq_get()`��ƥi�H�q�����W�@���U���h�ɪѲ���ơA�åB�H`tibble`�榡�x�s��ơA�����򪺸�ƳB�z��[��K�C���B�ܽd�p��U��2017/06/01��2018/05/31�A�E���B�x�n�q�B���عq�H�λO�W�[�v���ƪ����v�����ơC�b`tq_get()`��Ƥ����޼Ƭ�:

1. x: ���ĸ겣���N�X�A�ݰt�X��Ʒ��C
2. get: ��ƤU���ӷ��A���B�ڭ̳]�w�ѼƬ�`stock.price`�A�q[Yahoo Finance](https://finance.yahoo.com/)�U�����v�ѻ���ơC
3. from: ��ƤU���_�l��C
4. to: ��ƤU��������C

`tq_get()`��ƥi�U������ƨӷ��۷�h�A���F�ѻ���ƥ~�A�]���]�Ȥ�v����([Morningstar](https://www.morningstar.com/))�B�ѧQ�Ѯ����([Yahoo Finance](https://finance.yahoo.com/))���`�g���([FRED](https://fred.stlouisfed.org/))���A�u�n�ק��Ƥ���`get`�ѼƧY�i���o�C�ԲӤ��e�i�Ѧҭ�@�̪��������G[Core Functions in tidyquant](https://cran.r-project.org/web/packages/tidyquant/vignettes/TQ01-core-functions-in-tidyquant.html#get-quantitative-data)�C

�ڭ̦b[Yahoo Finance](https://finance.yahoo.com/)�n�U�����Ѳ��N�X���G�E��(2317.TW)�B�x�n�q(2330.TW)�Τ��عq�H(2412.TW)�λO�W�[�v����(^TWII)�A�{���X�g�k�p�U:


```r
# ���J�M��
library(tidyquant)

# �U�����
stockData <- c("^TWII", "2317.TW", "2330.TW", "2412.TW") %>%
  tq_get(get = "stock.price", from = "2017-06-01", to = "2018-05-31")

# �[�ݸ��
stockData
```

```
## # A tibble: 988 x 8
##    symbol       date     open     high      low    close  volume adjusted
##     <chr>     <date>    <dbl>    <dbl>    <dbl>    <dbl>   <dbl>    <dbl>
##  1  ^TWII 2017-06-01 10064.44 10100.37 10059.93 10087.42 1923600 10087.42
##  2  ^TWII 2017-06-02 10117.76 10152.53 10117.06 10152.53 2037600 10152.53
##  3  ^TWII 2017-06-03       NA       NA       NA       NA      NA       NA
##  4  ^TWII 2017-06-05 10164.89 10226.84 10164.89 10226.84 2141900 10226.84
##  5  ^TWII 2017-06-06 10213.17 10221.64 10190.39 10206.18 2016200 10206.18
##  6  ^TWII 2017-06-07 10216.14 10242.39 10183.15 10209.99 2172700 10209.99
##  7  ^TWII 2017-06-08 10215.93 10235.70 10211.00 10225.78 1703500 10225.78
##  8  ^TWII 2017-06-09 10238.55 10268.37 10198.80 10199.65 2139100 10199.65
##  9  ^TWII 2017-06-12 10137.04 10158.64 10109.96 10109.96 1746300 10109.96
## 10  ^TWII 2017-06-13 10109.70 10146.67 10109.70 10128.15 1586300 10128.15
## # ... with 978 more rows
```

²�檺���{���X�N�i�H�U���h�ɪѲ����v�ƾڡA�þ�z��tibble��Ʈ榡�A�P`quantmod`�M��`getSymbols()`��Ƭۤ�u���O��K�ܦh�C�M�Ӧ��@�Ӱ��D�O�A[Yahoo Finance](https://finance.yahoo.com/)�b�x�W�ѥ�����ƺ��@���ä��Ӧn�C�q�W���U�����ѻ���Ƥ��A�i�H�o�{2017-06-03�O�H�ʭȸ�Ƭ����A���x�Ѭ��ݤȸ`�s���P���ɥ����A[Yahoo Finance](https://finance.yahoo.com/)����Ʈw�o�S���O����A�o����O�����D���C�ҥH�ڭ̦b���x�W�ѥ����q�Ƹ�Ƥ��R�ɡA�ä��|�����q�����W�U����ơA�|�����q�]�ȸ�Ʈw�Ө��o��ơA�T�O��ƫ~��C�U�@�p�`�N�����p��Ū�J�~����ơA�þ�z��`tidyquant`�M���ϥΪ��榡�C

--------------------------------------------------

## �d�Ҹ�ƨӷ�

���F�z�L`tq_get()`��Ʀ�[Yahoo Finance](https://finance.yahoo.com/)�U����ƥ~�A�]�i�H�q�~����ƮwŪ�J�ƾڡA��z��`tidyquant`�һݭn����Ʈ榡�C���B�H�O�W�j�M�|�հ]���t�̱`�ϥΪ��x�W�g�ٷs����Ʈw(TEJ)���ҡA�z�L�S�����ɥ\���TEJ�U����ƿ�X��txt�ɮסA�M��A��R�n��Ū�J�ƾڡC��ƴ�����2017/06/01��2018/05/31�����W�վ��ѻ���ơC���R�겣�Ъ����O���E���B�x�n�q�B���عq�H�Ѳ��λO�W�[�v���ơC


```r
# Ū���ƾ�
stockData <- read.table("tej_data.txt", header = T, sep = "\t", stringsAsFactors = F) %>% 
  as_data_frame()

# ��z������(�̧Ǭ��Ѳ��N�X�B�W�١B����B�}�L���B�̰����B�̧C���B���L���B����q�Φ�����B)
colnames(stockData) <- c("code", "name", "date", "open", "high", "low", "close", "volume", "tradeValue")

# �N�Ѳ��N�X�ΦW�٪ťծ�R��
stockData <- stockData %>%
  mutate(code = gsub("\\s+","", code),
         name = gsub("\\s+","", name))

# �[�ݸ��
stockData
```

```
## # A tibble: 996 x 9
##     code     name     date     open     high      low    close  volume
##    <chr>    <chr>    <int>    <dbl>    <dbl>    <dbl>    <dbl>   <int>
##  1  2317     �E�� 20170601    99.57   100.53    99.09   100.53   27441
##  2  2330   �x�n�q 20170601   198.39   200.32   197.90   200.32   29623
##  3  2412   ���عq 20170601   103.13   103.60   102.65   103.13   10351
##  4 Y9999 �[�v���� 20170601 10064.44 10100.37 10059.93 10087.42 3935374
##  5  2317     �E�� 20170602   101.01   101.49   100.53   101.49   38194
##  6  2330   �x�n�q 20170602   201.77   202.26   200.81   202.26   23265
##  7  2412   ���عq 20170602   103.13   103.60   102.17   103.13    7341
##  8 Y9999 �[�v���� 20170602 10117.76 10152.53 10117.06 10152.53 4262071
##  9  2317     �E�� 20170603   101.01   101.49   100.53   101.01    9968
## 10  2330   �x�n�q 20170603   202.26   202.26   201.29   202.26    1535
## # ... with 986 more rows, and 1 more variables: tradeValue <int>
```

�ѩ�TEJ��Ʈw�ڭ̱ĥίS�����ɥ\���X�A�]������O�H8�X�Ʀr�榡�x�s�C���F��`tidyquant`�M�����B�@�A�ݱN������ѼƦr�榡�ର����榡�C


```r
# �N8�X�Ʀr����榡�ର����榡
DateConvert <- function(date){
  date <- as.Date(as.character(date), "%Y%m%d")
  return(date)
}

stockData <- stockData %>% mutate(date = DateConvert(date))

# �[�ݸ��
stockData
```

```
## # A tibble: 996 x 9
##     code     name       date     open     high      low    close  volume
##    <chr>    <chr>     <date>    <dbl>    <dbl>    <dbl>    <dbl>   <int>
##  1  2317     �E�� 2017-06-01    99.57   100.53    99.09   100.53   27441
##  2  2330   �x�n�q 2017-06-01   198.39   200.32   197.90   200.32   29623
##  3  2412   ���عq 2017-06-01   103.13   103.60   102.65   103.13   10351
##  4 Y9999 �[�v���� 2017-06-01 10064.44 10100.37 10059.93 10087.42 3935374
##  5  2317     �E�� 2017-06-02   101.01   101.49   100.53   101.49   38194
##  6  2330   �x�n�q 2017-06-02   201.77   202.26   200.81   202.26   23265
##  7  2412   ���عq 2017-06-02   103.13   103.60   102.17   103.13    7341
##  8 Y9999 �[�v���� 2017-06-02 10117.76 10152.53 10117.06 10152.53 4262071
##  9  2317     �E�� 2017-06-03   101.01   101.49   100.53   101.01    9968
## 10  2330   �x�n�q 2017-06-03   202.26   202.26   201.29   202.26    1535
## # ... with 986 more rows, and 1 more variables: tradeValue <int>
```

���U�ӧڭ̱N�H���d�Ҹ�ơA�Ӥ���`tidyquant`�M�󪺨�ƥΪk�C

--------------------------------------------------

## �p��޳N���мg�k�ܽd

���p�`�ܽd�p�󼶼g�޳N���СA�D�n�O�Q��`tq_mutate()`��ơA��޼ƨ̧Ǭ�:

1. data: ��ƶ��C
2. select: ��ܭp��޳N���Ш�Ʒ|�ϥΨ쪺������C
3. mutate_fun: ��ܭn�Ϊ��޳N���Ш��(`TTR`�M��)�C
4. �޳N���Ш�Ƥ��ѼƳ]�w�C

�z�L`group_by()`��Ʒf�t`tq_mutate()`��ƥH��`TTR`�M�󪺧޳N���Ш�ơA�Y�i��²�䪺�{���X�ֳt�a�p��X�U��Ѳ����޳N���ЭȡC�H�U���p��5��²�沾�ʥ����u�d�ҡG


```r
# �p��²�沾�ʥ����u�Ѽ�
stockData <- stockData %>%
  arrange(code, date) %>%         # ��ƱƧ�
  group_by(code) %>%              # �H�Ѳ��N�X���s�եؼ�
  tq_mutate(select = c(close),    # ��ܦ��L��
            mutate_fun = SMA,     # ���²�沾�ʥ����u
            n = 5) %>%            # 5��²�沾�ʥ����u�Ѽ�
  rename(ma5 = SMA)               # ���s�R�W���
  
# �[�ݸ��
stockData %>% 
  select(code, date, close, ma5) %>% 
  arrange(code, date) %>%
  na.omit()
```

```
## # A tibble: 980 x 4
## # Groups:   code [4]
##     code       date  close     ma5
##    <chr>     <date>  <dbl>   <dbl>
##  1  2317 2017-06-06 101.01 101.106
##  2  2317 2017-06-07 101.01 101.202
##  3  2317 2017-06-08 101.01 101.106
##  4  2317 2017-06-09 101.01 101.106
##  5  2317 2017-06-12  98.13 100.434
##  6  2317 2017-06-13  98.13  99.858
##  7  2317 2017-06-14  98.13  99.282
##  8  2317 2017-06-15  98.61  98.802
##  9  2317 2017-06-16 101.01  98.802
## 10  2317 2017-06-19 105.34 100.244
## # ... with 970 more rows
```

�p�G�n�A��10���20��²�沾�ʥ����u�A�h�~��V��s�W`tq_mutate()`:


```r
stockData <- stockData %>%
  
  # �p��10��²�沾�ʥ����u�Ѽ�
  tq_mutate(select = c(close),
            mutate_fun = SMA,
            n = 10) %>%
  rename(ma10 = SMA) %>%
  
  # �p��20��²�沾�ʥ����u�Ѽ�
  tq_mutate(select = c(close),
            mutate_fun = SMA,
            n = 20) %>%
  rename(ma20 = SMA)

# �[�ݸ��
stockData %>% 
  select(code, date, close, ma10:ma20) %>% 
  arrange(code, date) %>%
  na.omit()
```

```
## # A tibble: 920 x 5
## # Groups:   code [4]
##     code       date  close    ma10     ma20
##    <chr>     <date>  <dbl>   <dbl>    <dbl>
##  1  2317 2017-06-27 116.89 107.074 103.7780
##  2  2317 2017-06-28 113.52 108.613 104.4275
##  3  2317 2017-06-29 114.48 110.200 105.0770
##  4  2317 2017-06-30 112.56 111.355 105.6545
##  5  2317 2017-07-03 112.08 112.029 106.1840
##  6  2317 2017-07-04 108.71 111.885 106.5690
##  7  2317 2017-07-05 111.59 112.173 107.0980
##  8  2317 2017-07-06 111.11 112.461 107.6030
##  9  2317 2017-07-07 110.15 112.653 108.0600
## 10  2317 2017-07-10 111.11 112.220 108.7090
## # ... with 910 more rows
```

�Y�n�p���H�����СA�g�k��:


```r
stockData <- stockData %>%
  
  # �p���H������
  tq_mutate(select = c(high, low, close),   
            mutate_fun = stoch, 
            nFastK = 14, 
            nFastD = 3, 
            nSlowD = 3)

# �[�ݸ��
stockData %>% 
  select(code, date, fastK:stoch) %>% 
  arrange(code, date) %>%
  na.omit()
```

```
## # A tibble: 928 x 5
## # Groups:   code [4]
##     code       date     fastK     fastD     stoch
##    <chr>     <date>     <dbl>     <dbl>     <dbl>
##  1  2317 2017-06-23 0.8218263 0.8337045 0.8790184
##  2  2317 2017-06-26 0.9496104 0.8644210 0.8597810
##  3  2317 2017-06-27 0.9536008 0.9083458 0.8688238
##  4  2317 2017-06-28 0.7907202 0.8979771 0.8902480
##  5  2317 2017-06-29 0.8371194 0.8604801 0.8889343
##  6  2317 2017-06-30 0.7443209 0.7907202 0.8497258
##  7  2317 2017-07-03 0.7211213 0.7675205 0.8062403
##  8  2317 2017-07-04 0.5365112 0.6673178 0.7418528
##  9  2317 2017-07-05 0.6746362 0.6440895 0.6929760
## 10  2317 2017-07-06 0.5755668 0.5955714 0.6356596
## # ... with 918 more rows
```

`tq_mutate()`��Ƥ���`nFastK`�B`nFastD`��`nSlowD`�޼ƧY����`TTR`�M��`stoch()`���޼ơC�q�W������ƪ�i�H�o�{�A�z�L`tq_mutate()`��ơA�i�N`TTR`�M��`stoch()`��ƶ]�X��3����쵲�G(`fastK`�B`fastD`��`stoch`)�����s�W�b`stockData`��ƪ��C�Y�S��`tq_mutate()`�o�Ө�ơA��`mutate()`��ƭp���H�����з|�O��ܳ·Ъ��Ʊ��C

�Y�n�p��MACD���СA�g�k��:


```r
stockData <- stockData %>%

  # �p��MACD����
  tq_mutate(select = close,                
            mutate_fun = MACD, 
            nFast = 12, 
            nSlow = 26, 
            nSig  = 9)               

# �[�ݸ��
stockData %>% 
  select(code, date, macd:signal) %>% 
  arrange(code, date) %>%
  na.omit()
```

```
## # A tibble: 864 x 4
## # Groups:   code [4]
##     code       date     macd   signal
##    <chr>     <date>    <dbl>    <dbl>
##  1  2317 2017-07-17 3.399607 3.703507
##  2  2317 2017-07-18 3.414634 3.645732
##  3  2317 2017-07-19 3.385078 3.593601
##  4  2317 2017-07-20 3.286600 3.532201
##  5  2317 2017-07-21 3.066426 3.439046
##  6  2317 2017-07-24 2.928384 3.336914
##  7  2317 2017-07-25 2.855695 3.240670
##  8  2317 2017-07-26 2.661369 3.124810
##  9  2317 2017-07-27 2.617056 3.023259
## 10  2317 2017-07-28 2.551553 2.928918
## # ... with 854 more rows
```

�M�H�����мg�k�[�c�@�ˡA`tq_mutate()`��Ƥ���`nFast`�B`nSlow`��`nSig`�޼ƧY����`TTR`�M��`MACD()`���޼ơC

--------------------------------------------------

## �p���Z�ī��мg�k�ܽd

���ɧڭ̷|�Q�n�p��C�ӪѲ����Z�ī��СA�i��@�ǰ]�Ȥ��R(�Ҧp�غc���զX�ΪѲ�������)�C`tidyquant`�M�󧹬��a��X`PerformanceAnalytics`�M��A���ڭ̫ܤ�K�a�h�p���Z�ī��СC�b�p���Z�ī��ЮɡA�ڭ̻ݥ��N�U�ɪѲ��ѻ���ƾ�z�����S�v��ơA���B�~��z�X�O�W�[�v���Ƴ��S�v�����������S�v�A��ƾ�z�d�Ҧp�U�G


```r
# �p��U�겣���S�v
stockRet <- stockData %>% 
  select(code:date, close) %>%
  group_by(code) %>%
  arrange(code, date) %>%
  mutate(ret = close/lag(close)-1) %>%
  ungroup() %>%
  na.omit()

# ��z�������S�v
mktRet <- stockRet %>% 
  filter(code == "Y9999") %>%
  select(date, ret) %>%
  rename(mktRet = ret)
  
# ��z�U�겣���S�v�åB�֤J�U�����������������S�v
stockRet <- stockRet %>%
  select(code:date, ret) %>%
  filter(code != "Y9999") %>%
  left_join(mktRet, by = c("date" = "date"))
```

��z���᪺��ơA�C�Ӹ겣�b�C�ӥ���鳣������S�v�M���������������S�v�A�p�U�ҥܡG


```r
stockRet
```

```
## # A tibble: 744 x 5
##     code  name       date          ret        mktRet
##    <chr> <chr>     <date>        <dbl>         <dbl>
##  1  2317  �E�� 2017-06-02  0.009549388  0.0064545741
##  2  2317  �E�� 2017-06-03 -0.004729530  0.0005535566
##  3  2317  �E�� 2017-06-05  0.004752005  0.0067620581
##  4  2317  �E�� 2017-06-06 -0.004729530 -0.0020201744
##  5  2317  �E�� 2017-06-07  0.000000000  0.0003733032
##  6  2317  �E�� 2017-06-08  0.000000000  0.0015465245
##  7  2317  �E�� 2017-06-09  0.000000000 -0.0025553063
##  8  2317  �E�� 2017-06-12 -0.028512029 -0.0087934390
##  9  2317  �E�� 2017-06-13  0.000000000  0.0017992158
## 10  2317  �E�� 2017-06-14  0.000000000 -0.0054985363
## # ... with 734 more rows
```

���U�ӥܽd�p��p���Z�ī��СA�D�n�O�z�L`tq_performance()`��ơA��޼ƨ̧Ǭ�:

1. data: ��ƶ��C
2. Ra: �겣���S�v�C
3. Rb: ������ǳ��S�v�C
4. performance_fun: �Z�ī��Ш��(`PerformanceAnalytics`�M��)�C
5. �Z�ī��Ш�Ƥ��ѼƳ]�w�C 

�H�p��`�Ϊ��L����v���ҡA���B���]�L���I�~�Q�v��1%�A�{���g�k�p�U�C�ݪ`�N���a��O�A�p��L����v�ɤ��ݭn�Ψ쥫�����S�v�A�]��Rb���ѼƧڭ̵�NULL�ȡC


```r
sharpeRatio <- stockRet %>%
  group_by(code) %>%
  tq_performance(Ra = ret,
                 Rb = NULL,
                 performance_fun = SharpeRatio,
                 Rf = 0.01/252)

# �[�ݸ��
sharpeRatio
```

```
## # A tibble: 3 x 4
## # Groups:   code [3]
##    code `ESSharpe(Rf=0%,p=95%)` `StdDevSharpe(Rf=0%,p=95%)`
##   <chr>                   <dbl>                       <dbl>
## 1  2317             -0.02012416                 -0.03741787
## 2  2330              0.01323757                  0.03772705
## 3  2412              0.01668980                  0.03367462
## # ... with 1 more variables: `VaRSharpe(Rf=0%,p=95%)` <dbl>
```

�M`tq_mutate()`��Ƭ[�c�@�ˡA`tq_performance()`��Ƥ���`Rf`�޼Ƭ���`PerformanceAnalytics`�M��`SharpeRatio()`���޼ơC

�Y�n�]�ꥻ�겣�w���ҫ�(CAPM)�A�h�g�k��:


```r
capmTable <- stockRet %>%
  group_by(code) %>%
  tq_performance(Ra = ret, 
                 Rb = mktRet, 
                 performance_fun = table.CAPM,
                 Rf = 0.01/252)

# �[�ݸ��
capmTable
```

```
## # A tibble: 3 x 13
## # Groups:   code [3]
##    code ActivePremium  Alpha AnnualizedAlpha   Beta `Beta-` `Beta+`
##   <chr>         <dbl>  <dbl>           <dbl>  <dbl>   <dbl>   <dbl>
## 1  2317       -0.2291 -1e-03         -0.2167 1.3815  1.1093  1.5340
## 2  2330        0.0408  1e-04          0.0161 1.5010  1.3020  1.6403
## 3  2412       -0.0215  1e-04          0.0248 0.3600  0.3675  0.4613
## # ... with 6 more variables: Correlation <dbl>,
## #   `Correlationp-value` <dbl>, InformationRatio <dbl>, `R-squared` <dbl>,
## #   TrackingError <dbl>, TreynorRatio <dbl>
```

--------------------------------------------------

## ����W�v�ഫ

�W�z�p���Z�ī��ЮɬұĥΤ��W��ơA���@��`�����@�k�O�Τ��W��ƨӭp���Z�ī��СC�b`tidyquant`�M�󤤡A�ϥ�`tq_transmute()`��Ʒf�t�쥻`quantmod`�M�󤺪�`periodReturn()`��ơA�i�H�ܻ����a���ư��W�v�ഫ�C`tq_transmute()`���޼ƨ̧Ǭ�:

1. data: ��ƶ��C
2. select: ��ܸ�����C
3. mutate_fun: �M���ơC
4. col_rename: �s�W�����W�١C
5. �M���Ƥ��ѼƳ]�w�C


```r
# �ഫ�����W���
stockMonthRet <- stockData %>%
  group_by(code) %>%
  tq_transmute(select = close,
               mutate_fun = periodReturn,
               col_rename = "monthRet",
               period = "monthly")

# �[�ݸ��
stockMonthRet
```

```
## # A tibble: 48 x 3
## # Groups:   code [4]
##     code       date     monthRet
##    <chr>     <date>        <dbl>
##  1  2317 2017-06-30  0.119665771
##  2  2317 2017-07-31  0.043887704
##  3  2317 2017-08-31  0.000000000
##  4  2317 2017-09-30 -0.089361702
##  5  2317 2017-10-31  0.046728972
##  6  2317 2017-11-30 -0.107142857
##  7  2317 2017-12-29 -0.048000000
##  8  2317 2018-01-31 -0.031512605
##  9  2317 2018-02-27 -0.044468547
## 10  2317 2018-03-31  0.004540295
## # ... with 38 more rows
```

�p�G�Q�n�p��u�W�Φ~�W�A�u�n�b`period`�ѼƧ令`quarterly`��`yearly`�Y�i�G


```r
# �ഫ���u�W���
stockQuarterRet <- stockData %>%
  group_by(code) %>%
  tq_transmute(select = close,
               mutate_fun = periodReturn,
               col_rename = "monthRet",
               period = "quarterly")

# �[�ݸ��
stockQuarterRet
```

```
## # A tibble: 20 x 3
## # Groups:   code [4]
##     code       date     monthRet
##    <chr>     <date>        <dbl>
##  1  2317 2017-06-30  0.119665771
##  2  2317 2017-09-30 -0.049395878
##  3  2317 2017-12-29 -0.110280374
##  4  2317 2018-03-31 -0.070378151
##  5  2317 2018-05-31 -0.031638418
##  6  2330 2017-06-30  0.040834665
##  7  2330 2017-09-30  0.038369305
##  8  2330 2017-12-29  0.060046189
##  9  2330 2018-03-31  0.078431373
## 10  2330 2018-05-31 -0.094949495
## 11  2412 2017-06-30  0.000000000
## 12  2412 2017-09-30  0.013284204
## 13  2412 2017-12-29  0.014354067
## 14  2412 2018-03-31  0.066037736
## 15  2412 2018-05-31 -0.035398230
## 16 Y9999 2017-06-30  0.030498383
## 17 Y9999 2017-09-30 -0.001070700
## 18 Y9999 2017-12-29  0.024934659
## 19 Y9999 2018-03-31  0.025992074
## 20 Y9999 2018-05-31 -0.004078029
```


```r
# �ഫ���~�W���
stockYearRet <- stockData %>%
  group_by(code) %>%
  tq_transmute(select = close,
               mutate_fun = periodReturn,
               col_rename = "monthRet",
               period = "yearly")

# �[�ݸ��
stockYearRet
```

```
## # A tibble: 8 x 3
## # Groups:   code [4]
##    code       date    monthRet
##   <chr>     <date>       <dbl>
## 1  2317 2017-12-29 -0.05301900
## 2  2317 2018-05-31 -0.09978992
## 3  2330 2017-12-29  0.14566693
## 4  2330 2018-05-31 -0.02396514
## 5  2412 2017-12-29  0.02782895
## 6  2412 2018-05-31  0.02830189
## 7 Y9999 2017-12-29  0.05506264
## 8 Y9999 2018-05-31  0.02180805
```

--------------------------------------------------

## ø�s�ϧ�

`tidyquant`���F�N�]�Ȼ��M��P`dplyr`�M�󰵵��X�~�A�P`ggplot2`ø�ϮM��]��X�o�۷�n�A���U�ӱN�|�i�{�X�ӽd�ҡC

* ø�s�ѻ����W���չ�


```r
stockData %>%
  ggplot(aes(x = date, y = close, color = code)) +
  geom_line(size = 1) +
    labs(title = "Daily Stock Prices",
         x = "", y = "Close Prices", color = "") +
    facet_wrap(~ code, ncol = 2, scales = "free_y") +
    scale_y_continuous(labels = scales::dollar) +
    theme_tq() + 
    scale_color_tq()
```

<img src="tidyquant�M�󤶲�_files/figure-html/unnamed-chunk-15-1.png" style="display: block; margin: auto;" />

* ø�s�޳N���R�ϧ�(�H�x�n�q����)


```r
stockData %>%
  filter(code == "2330") %>%
  ggplot(aes(x = date, y = close)) +
  geom_candlestick(aes(open = open, high = high, low = low, close = close),
                   color_up = "firebrick3", color_down = "chartreuse3", 
                   fill_up  = "firebrick3", fill_down  = "chartreuse3") +
  labs(title = "2330 Candlestick Chart", y = "Closing Price", x = "") + 
  theme_tq() +
  scale_x_date(expand = c(0, 0))
```

<img src="tidyquant�M�󤶲�_files/figure-html/unnamed-chunk-16-1.png" style="display: block; margin: auto;" />

* ø�s�޳N���R�ϧ�(�H�x�n�q����)��5��B10���20�駡�u


```r
stockData %>%
  filter(code == "2330") %>%
  ggplot(aes(x = date, y = close)) +
  geom_candlestick(aes(open = open, high = high, low = low, close = close),
                   color_up = "firebrick3", color_down = "chartreuse3", 
                   fill_up  = "firebrick3", fill_down  = "chartreuse3") +
  geom_ma(ma_fun = SMA, n = 5, color = "blue", linetype = 7,size = 1) +
  geom_ma(ma_fun = SMA, n = 10, color = "orange", linetype = 7, size = 1) + 
  geom_ma(ma_fun = SMA, n = 20, color = "green", linetype = 7, size = 1) +
  labs(title = "2330 Candlestick Chart", y = "Closing Price", x = "") + 
  theme_tq() +
  scale_x_date(expand = c(0, 0))
```

<img src="tidyquant�M�󤶲�_files/figure-html/unnamed-chunk-17-1.png" style="display: block; margin: auto;" />

* ø�s�޳N���R�ϧ�(�H�x�n�q����)�Υ��L�q�D


```r
stockData %>%
  filter(code == "2330") %>%
  ggplot(aes(x = date, y = close, open = open, high = high, low = low, close = close)) +
  geom_candlestick(color_up = "firebrick3", color_down = "chartreuse3", 
                   fill_up  = "firebrick3", fill_down  = "chartreuse3") +
  geom_bbands(ma_fun = SMA, sd = 2, n = 20, 
              linetype = 7, size = 1, alpha = 0.2,
              fill = palette_light()[[1]],
              color_bands = palette_light()[[1]],
              color_ma = palette_light()[[2]]) +
  labs(title = "2330 Candlestick Chart", y = "Closing Price", x = "") + 
  theme_tq() +
  scale_x_date(expand = c(0, 0))
```

<img src="tidyquant�M�󤶲�_files/figure-html/unnamed-chunk-18-1.png" style="display: block; margin: auto;" />

--------------------------------------------------

## ���y

�q�W�z���d�Ҥ��A�i�H�ݨ�`tidyquant`�M��ܴΦa�N�]�ȮM��P`tidyverse`�M�󧹬��a���X�C���ΦA�g�Ӧh�������{���M�j��A¶��¶�h�a�h�p��C��Ѳ����޳N���ЩM�Z�ī��СC�o�ӮM�󪺾�X�A����R�y�����]�Ȥ��R���ϥΪ̨ӻ��u�O�@�j�֭��I���g�峹���^��`tidyquant`�M��̭��n�������A����@�̼��g�������峹�٦���h�Ӹ`�����ΡA��󦹮M�󦳿��쪺Ū�̡A��ĳ�i�h�I�\�ӬݡC




