
# Login request

```curl
curl --request POST \
  --url https://grindr.mobi/v5/sessions \
  --compressed \
  --header 'accept: application/json' \
  --header 'accept-encoding: gzip' \
  --header 'accept-language: en-US' \
  --header 'connection: Keep-Alive' \
  --header 'content-type: application/json; charset=UTF-8' \
  --header 'host: grindr.mobi' \
  --header 'l-device-info: ac3d25ddc7d31a8c;GLOBAL;2;7982997534;2276x1080;00000000-0000-0000-0000-000000000000' \
  --header 'l-locale: en_US' \
  --header 'l-time-zone: Europe/Oslo' \
  --header 'requirerealdeviceinfo: true' \
  --header 'user-agent: grindr3/25.5.0.136635;136635;Free;Android 14;22021211RG;Xiaomi' \
  --data '{"email":"[EMAIL]","password":"[PASSWORD]","token":"","geohash:""}' 
```

returns
```
{"profileId":"570525909","sessionId":"[BASE64].[BASE64 (contains features)].[TOKEN]","xmppToken":"[BASE 64 ENCODED DATA].[BASE 64 ENCODED DATA].[TOKEN]","authToken":"[AUTHTOKEN]"}
```


The firebase token will work even if it has been modified or is blank:
```
euY8_yFrQYiVqor_4YQfoK:APA91bGxm4iOVAMQ8BSCJzSRE06IGj_EKs1kihEUgkuo7f8Y2nyHuclWX2SSC0IkuzZOzjcHXwRi9yoLth6TP4s8P7mbw5DiUS1pqtT9qu55HFIJ1dgYoC-CCPXsTvI_XWXPoDOxtlI_
```
# Get Users
```
curl --request GET \
  --url_v3 'https://grindr.mobi/v3/cascade?nearbyGeoHash=6gytbnpe1y21&onlineOnly=true&photoOnly=false&faceOnly=false&notRecentlyChatted=false&sexualPositions=1&fresh=false&pageNumber=1&genders=1&favorites=false&showSponsoredProfiles=false&shuffle=false' \
  --compressed \
  --header 'accept: application/json' \
  --header 'accept-encoding: gzip' \
  --header 'accept-language: en-US' \
  --header 'authorization: Grindr3 [AUTHTOKEN]' \
  --header 'connection: Keep-Alive' \
  --header 'host: grindr.mobi' \
  --header 'l-device-info: 2938f76cff50af57;GLOBAL;2;2069590016;2277x1080;a9ffffa4-2b0e-479d-b3db-ae117c0a9686' \
  --header 'l-grindr-roles: []' \
  --header 'l-locale: en_US' \
  --header 'l-time-zone: Europe/Oslo' \
  --header 'user-agent: grindr3/25.5.0.136635;136635;Free;Android 14;22021211RG;Xiaomi'
```
