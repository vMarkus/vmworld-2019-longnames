Reqs: Linux or similar shell required

so you downloaded all VMworld 2019 videos and have shortnames like "ADV1045BU.mp4"

download 
```
mappings.txt
```
file to directory, where all the video files reside and run
```
awk -F';' 'system("mv " $2 " " $1)' mapping.txt
```
you are welcome ;-)
