---
title: Prism, Illinois Tech's LGBTQ+ Club
layout: splash
logo: /assets/images/logos/pride_logo.png
header:
  text: Illinois Tech's LGBTQ+ Club
  inverted_splash: true
  inverted_menu: true
  overlay_image: /assets/images/headers/pride_background.jpg
  actions:
    - label: Join us on HawkLink
      url: https://hawklink.iit.edu/organization/Prism
---

<link href='assets/packages/core/main.css' rel='stylesheet' />
<link href='assets/packages/daygrid/main.css' rel='stylesheet' />
<link href='assets/packages/list/main.css' rel='stylesheet' />

## Prism

Prism is Illinois Tech's LGBTQ+ club on campus. The purpose of Prism at IIT is to create a community on campus for all students, faculty, and staff within the LGBTQIA+ community and offer support for those who are questioning their sexual and/or gender identities. Through dialogues, fellowship, and social activities, our objective is to raise awareness about the important issues the LGBTQIA+ community faces and foster an accepting campus environment.  

### GBM

For Spring 2019, our General Body Meetings will be **Wednesdays at 6PM in Pritzker (Life Sciences) 152**

<div id='loading'>loading...</div>
<div id='calendar'></div>

### Links

[Add our events to your Google Calendar](https://calendar.google.com/calendar/b/0/r?cid=iit.edu_687jcqqckknee6rg7fcn6n4ess@group.calendar.google.com)

[HawkLink](https://hawklink.iit.edu/organization/Prism) - Join our mailing list!

Email us at [prism@iit.edu](mailto:prism@iit.edu)

<script src='assets/packages/core/main.js'></script>
<script src='assets/packages/interaction/main.js'></script>
<script src='assets/packages/daygrid/main.js'></script>
<script src='assets/packages/list/main.js'></script>
<script src='assets/packages/google-calendar/main.js'></script>
<script>

document.addEventListener('DOMContentLoaded', function() {
    var calendarEl = document.getElementById('calendar');

    var calendar = new FullCalendar.Calendar(calendarEl, {

    plugins: [ 'interaction', 'dayGrid', 'list', 'googleCalendar' ],

    header: {
        left: 'prev,next today',
        center: 'title',
        right: 'dayGridMonth,listYear'
    },

    displayEventTime: true, // don't show the time column in list view

    googleCalendarApiKey: 'AIzaSyCHN6dNi72HpEkLBZnpqnlB7jZx3tKgmzQ',

    events: 'iit.edu_687jcqqckknee6rg7fcn6n4ess@group.calendar.google.com',

    eventClick: function(arg) {
        // opens events in a popup window
        window.open(arg.event.url, 'google-calendar-event', 'width=700,height=600');

        arg.jsEvent.preventDefault() // don't navigate in main tab
    },

    loading: function(bool) {
        document.getElementById('loading').style.display =
        bool ? 'block' : 'none';
    }

    });

    calendar.render();
});

</script>
