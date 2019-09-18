Reqs: Linux or similar shell required

so you downloaded all VMworld 2019 videos with Dominiks single line command and William Lams [@lamw](https://github.com/lamw) link list at https://github.com/lamw/vmworld2019-session-urls

````
# load Session Catalog (login required)
curl https://raw.githubusercontent.com/lamw/vmworld2019-session-urls/master/us.txt > us.txt
# download Content, added continue, just in case download breaks and you can rerun
awk -F# '{print $2}' us.txt | while read x; do wget -c --referer http://www.vmware.com $x; done
````

and have shortnames like "ADV1045BU.mp4"

download 
```
mappings.txt
```
file to directory, where all the video files reside and run
```
awk -F';' 'system("mv " $2 " " $1)' mapping.txt
```
you are welcome ;-)
