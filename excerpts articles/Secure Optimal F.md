[[Optimal F]] is a [[money management]] [[strategy]] that can be used to improve and maximize system's performance by finding the best percent of capital to invest in each trade.

The concept of percent or fractional strategy itself comes from the [[Kelly formula]], which estimates the percentage of your [[capital]] to trade when the amounts won and lost are not equal:

>*f = ((b+1)p - 1))/b*
*b* = Ratio of the size won on a winning bet to the size lost on
a losing bet
*p* = Probability of a winning bet

A simple example would be if you had three bets — two winners and one loser (1, 1, zero) — and you made or lost equal amounts:
f = ((1+1)0.666-1)1 = 0.33333

This formula solves for f. This formula is applicable when there are only two outcomes. For traders, there are many outcomes. Vince introduces optimal f, and to find the value of optimal f, we need to maximize what Vince calls terminal wealth relative (TWR). The problem can be formulated thus:

>*TWR(f) -> max*
where *TWR(f)=(HPR1(f))((HPR2(f))(...(HPRn(f))*
*HPRi(f)=1+(f((-Return on the trade i)/(Return on the
worst losing trade))*
*HPR* = Holding period return

The following are the results in each series of your game:

>Series 1=*{1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 1}*
Series 2=*{0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1}*
Series 3=*{1, 0, 1, 0, 1, 0, 1, 0, 1, 0, 0}*

Now, let’s say you have $100,000. Let us find the optimal f based on the outcomes 1, 1, and zero. You had trades of USD 500,  USD 500, and - USD 500:

>*HPR1=(1+f(500/500))*
*HPR2=(1+f(500/500))*
*HPR3=(1-f(500/500))*

That gives us the expression for TWR:

>*TWR=(1+f)(1+f)(1-f)=1+f-f^2-f^3*

This function reaches the maximum at *f = 1/3*. This means that
optimal f tells you to invest in every trade a third of your
money, which for the first trade would be $33,333.

[Vince](https://atas.net/volume-analysis/kelly-formula/) added new concepts:

-   **HPR (holding period returns)** is the rate of return for any trade + 1. That is, the number is >1 for profitable trades and – <1 for loss-making ones. For example, 10% profit will be considered as 1.1, while 25% loss will be considered as 0.75. HPR should be calculated for every trade:

>HPR = 1 + f \* (-T / BL)
F – the fixed capital share;
T – profit/loss in a trade with the opposite sign, which means that the loss becomes a positive number while profit becomes a negative number.
BL – the biggest loss in a series is always a negative value.

-   **TWP (terminal wealth relative)** is the aggregate income of the trader trades in the form of an accumulation factor, that is multiplication of all HPR.

For example, TWP=15.69 means that the start-up capital was increased 15.69 times.
While looping f in the range from 0.1 to 1, you may find the number, which will produce the highest TWP for the trading system. It could be done in Excel.