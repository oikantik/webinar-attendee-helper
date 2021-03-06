![Demo](https://dl.dropboxusercontent.com/s/rbqlvwsquaifz1e/advanced.png)

This is a package for StealthSeminar users for showing webinar date and time, countdown, event and calendar .

1. Where ever you use this, make sure you are passing the attendee id, otherwise it will not work. e.g. if you are using it on `https://yoursite.com` you can go to StealthSeminar and set this as thank you page url, which will take care of it for you, `https://yoursite.com/?autoLoginId={autoLoginId}`

2. Add this to the header section of your page

```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/oikantik/webinar-attendee-helper@1.0.0/attendee-information.css">
```

3. This package is dependent on DayJS heavily. These are the dependencies:

```
<script src="https://unpkg.com/dayjs@1.10.4/dayjs.min.js"></script>

<script src="https://unpkg.com/dayjs@1.10.4/plugin/utc.js"></script>

<script src="https://unpkg.com/dayjs@1.10.4/plugin/timezone.js"></script>

<script src="https://unpkg.com/dayjs@1.10.4/plugin/advancedFormat.js"></script>

<!-- AddEvent script : This is only needed if you want to add an add to calendar event -->
<script type="text/javascript" src="https://addevent.com/libs/atc/1.6.1/atc.min.js" async defer></script>
```

If you are using AddEvent, please make sure you have signed up with them and verified your domain where these widgets would be.

Make sure to put these before the end of the body section.

4. And then add this package.

```
<script src="https://cdn.jsdelivr.net/gh/oikantik/webinar-attendee-helper@1.0.0/attendee-information.js"></script>
  <script>
    webinar.shortId = "XXXXX"; // replace this with your shortid
    webinar.event.summary = ''; // if you are using calendar
    webinar.event.description = ""; // if you are using calendar
    webinar.loadContainers();
    webinar.request([calendarNode, textNode, countdownNode, addEventNode], errorNode);
    webinar.linkNode();
  </script>
```

5. Now you can use these
```
<!-- for showing text date time -->
<div class="ss-datetime"></div>

<!-- for showing calendar date time -->
<div class="ss-calendar"></div>

<!-- for showing countdown -->
<div class="ss-countdown"></div>

<!-- for showing webinar link -->
<div class="ss-links"></div>

<!-- for showing event -->
<div class="ss-event-calendar">
```
