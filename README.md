# ios-ads-json-files

### Manual Ad unit Replacement process

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



test
