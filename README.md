# Risk Region

Program based on [RiskLevel](https://github.com/KaikePing/RiskLevel), use mongoDB to store risk region information from offical website, and send notice email to specific addresss.

`passwd.py` is the config file contain mail sending account and receiving address:

```python
# sending config
account = 'sending@email.com'
passwd = 'PASSWORD'

# receiver info
receiver = 'receiving@email.com'
```

Email are sending using [zmail](https://github.com/zhangyunhao116/zmail) moudule, so stmp server are parsed automaticly, only mail account and password are needed.

# REQUIREMENT

- mongoDB
- python3
    + pymongo
    + schedule
    + zmail
    + pandas
    + requests

Please notice that `zmail` is only available through pip

# HOW TO USE

1. Clone this project
2. Install the requirements
3. Create `passwd.py`, and config the sending account and reciving account
4. Start mongoDB
5. Start `risk_region.py`

# TODO

- [ ] A CUI to config mail infomation and start the service
- [ ] Automatic database init process, this should to be done using `insert.py` manually now
- [ ] Simple plotly app to display the risk region trend or something
- [ ] A more decent `config.py`