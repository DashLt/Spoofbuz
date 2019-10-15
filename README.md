# LEGAL NOTES: 
This repository does not publish any of Qobuz's private secrets or app IDs. It contains regular expressions and other code to dynamically grab them from Qobuz's web player's *publicly available*  JavaScript, which is not rehosted, but grabbed client side. S craping public data is not a violation of the Computer Fraud and Abuse Act (USA) according to the Ninth Court of Appeals, [case # 17-16783](http://cdn.ca9.uscourts.gov/datastore/opinions/2019/09/09/17-16783.pdf) (see page 29). 

---

# Spoofbuz
A library for spoofing the Qobuz web player.  
This is not intended for end users.

# Usage:

```py
import spoofbuz
spoofer = spoofbuz.Spoofer()
appId = spoofer.getAppId() # returns 9 digit app ID
secrets = spoofer.getAppSecrets() # returns all possible app secrets listed in bundle.js, sorted by likeliest to work
best_secret = list(secrets.values())[0] # first secret: this should work most of the time
```
