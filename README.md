7. Create a venv (different from chia-rosechain) and start the pool server using the following commands:

```
cd rose-garden
python3 -m venv ./venv
source ./venv/bin/activate
pip install ../chia-rosechain/ 
sudo CHIA_ROOT="/your/home/dir/.chiarose/mainnet" ./venv/bin/python -m pool
```

You should see something like this when starting, but no errors:
```
INFO:root:Logging in: {'fingerprint': 2164248527, 'success': True}
INFO:root:Obtaining balance: {'confirmed_wallet_balance': 0, 'max_send_amount': 0, 'pending_change': 0, 'pending_coin_removal_count': 0, 'spendable_balance': 0, 'unconfirmed_wallet_balance': 0, 'unspent_coin_count': 0, 'wallet_id': 1}
```

8. Create a pool nft (on the farmer key) by doing `chia plotnft create -s pool -u https://127.0.0.1:80`, or whatever host:port you want
to use for your pool. Approve it and wait for transaction confirmation. This url must match *exactly* with what the 
   pool uses.
   
9. Do `chia plotnft show` to ensure that your plotnft is created. Now start making some plots for this pool nft.
You can make plots by specifying the -c argument in `chia plots create`. Make sure to *not* use the `-p` argument. The 
    value you should use for -c is the `P2 singleton address` from `chia plotnft show` output.
 You can start with small k25 plots and see if partials are submitted from the farmer to the pool server. The output
will be the following in the pool if everything is working:
```
INFO:root:Returning {'new_difficulty': 1963211364}, time: 0.017535686492919922 singleton: 0x1f8dab79a614a82f9834c8f395f5fe195ae020807169b71a10218b9788a7a573
```
    
Please send a message to @sorgente711 on keybase if you have questions about the 9 steps explained above. All other questions
should be send to the #pools channel in keybase. 

 
