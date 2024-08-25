# Installing environmental requirements

To set the app you need to run these commands in the console (Windows):

```sh
python3 -m venv crypto_test
.\crypto_test\Scripts\activate
pip3 install -r requirements.txt
```

# Notebook description (all_currencies_scrapp)

- This application runs a web scraping script to extract information about a given set of cryptocurrencies:
    - Bitcoin.
    - Jupiter.
    - TARS AI.
    - Solana.
    - Ethereum.
    - XRP.
    - Kaspa.
    - Notcoin.

- Scrapping elements:
    - Price.
    - Market cap.
    - Scrapping timestamp.

- You can set the time of execution of the notebook (minutes and seconds) and the time interval between scraping loops through an input below this code field:
```sh
print('''Set execution time or use default lapses (1 hour)?:
      1. Set
      Anything else. Use default
      ''')
choose = input()

if choose == '1':
    # setting execution time
    print('Set time of execution:')
    print ('Set minutes')
    minutes = input()
    minutes = int(minutes)
    print ('Set seconds')
    seconds = input()
    seconds = int(seconds)
    timeout = time.time() + minutes + seconds
    print(f'Execution time = {minutes}:{seconds}')
    timeout = time.time() + ((minutes*60) + seconds)

    # setting intervals
    print('Set time interval between scrapping loops:')
    print ('Set minutes')
    iminutes = input()
    iminutes = int(iminutes)
    print ('Set seconds')
    iseconds = input()
    iseconds = int(iseconds)
    print(f'interval time = {iminutes}:{iseconds}')
    interval = (iminutes*60) + iseconds
else:
    timeout = time.time() + 60*60
    interval = 150
```

- Finally, the results of the scraping records will be charted.