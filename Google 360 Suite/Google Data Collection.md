### How Google Analytics Collect Our Data

Google Website Tag Manager

```html
  <head>
  <!-- Global site tag (gtag.js) - Google Analytics -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-FVYR6PTCH9"></script>
    <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-FVYR6PTCH9');
    </script>
  </head>
```

### Whenever we Run a Website this Script is Triggered and it Collects Data.

### Hits ( Page Tracking, Event Tracking, Ecommerce Tracking and Social Interactions )

### Payload | Package ( Key Insights : Browser Language, Page Name, Screen Resolution )

### dl : Document Location ( https://shop.google.com )

### dr : Document Referrer ( https://www.google.com )

### dt : Document Title ( Page Title : Home )

### sr : Screen Resolution  ( User is using Desktop, Mobile or Tablet )

### vp : Viewport Size ( 645 x 574 )

### t : Hit Type ( event )

### tid : Tracking ID ( UA-54516992-1 or GA-4 ) UA : Universal Analytics

### ec : Event Category ( Video, Image, Article )

### ea : Event Action ( play, open, zoom, read )

### el : Event Label ( Event is on Homepage or any other page of Website )

### cd : Custom Dimension ( view completion : Video is watched completely or just opened and closed )

### cm : Custom Metric ( view time : Amount of Time User Watched the Video )

### cid : Unique Client ID ( ID Measures how many times user access the Website )

> Unique Client ID is not Tracked in Icognito Mode ( Each and Every Time the User is a Fresh | New User ) 

> User Browser Cookie is Maintained

> User can be Identified across Multiple Session, Cross Browser ( Chrome, Edge, Safari ), Cross Platform ( Windows, Linux, IOS ) and Cross Device ( Mobile, Tablet, Desktop, TV )

> Every New User is Associated with Unique Google Client ID.
