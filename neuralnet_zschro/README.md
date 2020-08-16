# gekko-neuralnet
Neural network strategy for Gekko

This strategy was inspired from Mounir's strategy, found on the Gekko Discord channel. 
For reference, that's the original work: https://github.com/cloggy45/Gekko-Bot-Resources/blob/master/gekko/strategies/mounirs-ga-version-2.js

# Install
copy the file(s) from /strategies/ into the strategies folder of your gekko install
copy the file(s) from /toml/ into the /config/strategies/ folder of your gekko install

Install the modules in your gekko folder:
`npm install convnetjs mathjs`

# Usage / Configuration

```javascript
// the neural network training method to use. Options are 'sgd', 'adagrad', 'windowgrad', 'nesterov'
method = 'adadelta'

// the treshold for buying into a currency. e.g.: The predicted price is 1% above the current candle.close

threshold_buy = 1.00

// the treshold for selling a currency. e.g.: The predicted price is 1% under the current candle.close
threshold_sell = -1.00

// The length of the candle.close price buffer. It's used to train the network on every update cycle.
price_buffer_len = 100

// The learning rate of net - not used for adadelta or adagrad
learning_rate = 0.01


// learning speed - not used for adadelta or adagrad
momentum = 0.9
//l2 decay
decay = 0.1

//minimum number of prictions until the network is considered 'trained'. History size should be equal
min_predictions = 720

//enables stoploss function
stoploss_enabled = false

//trigger stoploss 5% under last buyprice
stoploss_threshold = 0.95

```

If this strategy is useful for you and generates profits. Buy me a coffee, or two:
 
ETH 0xeb969152217062760104b2e17545647e05f1673b

BTC 16k9vwf4vDfF9ufnuu91WDjheVokPjh2X4

NANO xrb_3boer7rzaewcn583jrfid687znn5ncagp7tqi97pjnupxpr8ep6aor1dqrzy
