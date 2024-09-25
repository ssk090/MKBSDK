# MKBSDK
- A script to get all the HD wallpapers from planes app
```
URL="https://storage.googleapis.com/panels-api/data/20240916/media-1a-i-p~s"
curl -s $URL | jq -r '.data[] | select(has("dhd")) | .dhd' | while read -r url; do
filename=$(basename "${url%%\?*}")
curl -s -o "$filename" "$url"
done
```


### To check the total number of files
ls | wc -l

### Interesting Project
- https://jsfiddle.net/hkb6pL20/
