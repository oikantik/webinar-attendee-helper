This is a package for StealthSeminar users for showing webinar date and time, countdown, event and calendar .

Add this to the header section of your page

```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/oikantik/webinar-attendee-helper/attendee-information.css">
```

This package is dependent on DayJS heavily. These are the dependencies:

```
<script src="https://unpkg.com/dayjs@1.10.4/dayjs.min.js"></script>

<script src="https://unpkg.com/dayjs@1.10.4/plugin/utc.js"></script>

<script src="https://unpkg.com/dayjs@1.10.4/plugin/timezone.js"></script>

<script src="https://unpkg.com/dayjs@1.10.4/plugin/advancedFormat.js"></script>
```

Make sure to put these before the end of the body section.

And then add this package.

```
<script src="https://cdn.jsdelivr.net/gh/oikantik/webinar-attendee-helper/attendee-information.js"></script>
  <script>
    webinar.shortId = "XXXXX"; // replace this with your shortid
    webinar.loadContainers();
    webinar.request([calendarNode, textNode, countdownNode, addEventNode], errorNode);
    webinar.linkNode();
  </script>
```

Now you can use these
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
