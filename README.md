# ios-ads-json-files

### Ad unit replacement with Github

* Open https://github.com/SuperUnlimited/ios-ads-json-files
* Click on the ads folder
* Click on the file name what we need to modify
* Click on the Edit pencil symbol
* Modify file with required changes (ad unit ids)
* Give Commit message as Jir Ticket Number and Title
* Click on Commit changes.
* Now Jenkins Job Alerts will get to our slack channel
* Should get a Success message and if we get any error message please inform to DevOps team
* Check changes After 1hr ( Because of Cloudflare cache)

https://docs.google.com/document/d/1eN0DrrzDR6DU9xx17TzB9OCVmyGsZzpW5qZkvstwWvc/edit?usp=sharing

#### check

https://www.mobilejump.mobi/tizi_ads/freetizi1.json

https://www.mobilejump.mobi/tizi_ads/freetizi2.json

https://www.mobilejump.mobi/tizi_ads/freetizi3.json

https://www.mobilejump.mobi/tizi_ads/tizi1.json

https://www.mobilejump.mobi/tizi_ads/tizi2.json

https://www.mobilejump.mobi/tizi_ads/tizi3.json

### Manual Ad unit Replacement process with server

Connect to mobilejump Server(167.71.45.40) with tizi_ads user
##### ads json files location
```cd /home/wwwroot/default/tizi_ads```
##### backup of json files
```mkdir /home/tizi_ads/tizi_ads_backup_$(date +"%d-%m-%Y") ; cp /home/wwwroot/default/tizi_ads/* $_```

##### find the data in files
```grep 'ca-app-pub-3509434118277818/7554047032' *.json```

##### Modify/Replace the data in files

Use vi editor or sed command to replace the ad unit ids

```sed -i 's|ca-app-pub-3509434118277818/5524976962|ca-app-pub-3509434118277818/9426974201|g' *.json```

#### check

https://www.mobilejump.mobi/tizi_ads/freetizi1.json

https://www.mobilejump.mobi/tizi_ads/freetizi2.json

https://www.mobilejump.mobi/tizi_ads/freetizi3.json


