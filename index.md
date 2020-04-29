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

<div class="ui two column doubling stackable grid container" style="margin-bottom: 14px;">
<div class="ui raised very padded container segment column">
<h2>Welcome to Prism</h2>
<p>
Prism is Illinois Tech's LGBTQ+ club on campus. The purpose of Prism at IIT is to create a community on campus for all students, faculty, and staff within the LGBTQIA+ community and offer support for those who are questioning their sexual and/or gender identities. Through dialogues, fellowship, and social activities, our objective is to raise awareness about the important issues the LGBTQIA+ community faces and foster an accepting campus environment.  
</p>
</div>
<div class="ui raised very padded container segment column" style="margin-top: 0px;">

<a href="https://calendar.google.com/calendar/b/0/r?cid=iit.edu_687jcqqckknee6rg7fcn6n4ess@group.calendar.google.com" class="fluid ui button" style="margin-bottom: 14px;">Add our events to your Google Calendar</a>

<div data-tooltip="Both options will get all of our emails, but you can choose either for privacy reasons.">
<h4 style="margin-bottom: 0px; text-align: center;">Join our Mailing list through</h4>
<div class="fluid ui buttons" style="margin-bottom: 26px;">
    <a href="https://hawklink.iit.edu/organization/Prism" class="ui primary button">HawkLink</a>
    <div class="or"></div>
    <a href="https://groups.google.com/forum/#!forum/prism-iit/join" class="ui button">Google Groups</a>
</div>
</div>

<div class="ui fluid animated fade button" tabindex="0">
    <div class="visible content">Get in touch with us through email</div>
    <a href="mailto:prism@iit.edu" class="hidden content">
        prism@iit.edu
    </a>
</div>
</div>


<div class="ui message">
    For Spring 2020, our General Body Meetings (GBMs) will be in Pritzker (Life Sciences) Room 152. We hope to see you there!
</div>

<div id='loading'>loading...</div>
<div id='calendar'></div>


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
