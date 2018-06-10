Objective: To increase the accessibiliy lighthouse score. When running google maps API an iframe gets generated that doesn't have a proper title. This script will insert the title. 

Note: I have not tested this, but it's from a user on Slack:

dseet (MWS) [8:14 PM]
commented on @Tanya [MWS]’s file image.png: Not required for Stage 1 to be accepted but if you are one of those pesky Devs like me. You can put the following in the InitMap function in both HTML files

```
 google.maps.event.addListenerOnce(self.map, 'idle', () => {
    document.getElementsByTagName('iframe')[0].title = "Google Maps";
  });
```
