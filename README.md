# intel_invest
> A package to obtain the relevant figures for a company and apply some rules of thumb precribed in the book Intelligent Investor, by Benjamin Graham.


## Install

`pip install intel_invest`

## How to use

To obtain Graham's opinion on `Abbott Laboratories` do the following:

```python
stock = Stock("ABT")
```

Ben will ask two questions:

- is price < 25 * average 5 year earning per share
- is price to earning ratio * price to book value < 22.5

```python
# question 1 is answered by 
stock.will_ben_buy_1()
```




    False



```python
# question 2 is answered by 
stock.will_ben_buy_2()
```




    False



```python
# to obtain the current price
stock.get_price()
```




    117.2



```python
# obtain the last 5 years of earning per share
stock.get_esp()
```




    [0.93, 0.27, 1.34, 2.07, 2.52]



```python
# obtain Graham's recommended maximum stock price
stock.max_price()
```




    35.65



In this case one will be advised not to buy this Stock as it is too expensive. 
