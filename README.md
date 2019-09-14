# HTML
<html>
<title>
    Dumb Ways to Mine - Districts Page 
</title> 
<header>
    <script src="JS/jquery-3.4.1.min.js.js"></script>
    <script src="images.js"></script>

    <link rel="stylesheet" href="style2.css">
</header>
<body>
    <div id="Districts">
    <div class="DistrictChartersTowers"> 
        <img src="" alt="">
        <h1>Charter's Towers</h1>
    </div>
    <a href="blank">
    <div class="DistrictIpswitch"> 
            <img src="" alt="">
            <h1>Ipswich</h1>
            <h2> </h2>
    </div>
</a>
    <div class="DistrictOtherMine"> 
            <h1>Other mine</h1>
        <img src="" alt="">
    </div>
      

</div>
</body>
</html>

#JS
 /*Script from StacksOverflow */ 
 console.log("loading");

 $(document).ready(function(){
    console.log("loading");
    var keyword = 'mining'
     $.getJSON("http://api.flickr.com/services/feeds/photos_public.gne?jsoncallback=?",
    {
        tags: keyword,
        tagmode: "any",
        format: "json"
     },
     function(data) {
         console.log("function data");
         var rnd = Math.floor(Math.random() * data.items.length);

         var image_src = data.items[rnd]['media']['m'].replace("_m", "_b");

         $('.DistrictIpswitch').css('background-image', "url('" + image_src + "')");


     });
     var keyword = 'mining'
     $.getJSON("http://api.flickr.com/services/feeds/photos_public.gne?jsoncallback=?",
     {
         tags: keyword,
         tagmode: "any",
         format: "json"
      },
      function(data) {
          console.log("function data");
          var rnd = Math.floor(Math.random() * data.items.length);
 
          var image_src = data.items[rnd]['media']['m'].replace("_m", "_b");
 
          $('.DistrictChartersTowers').css('background-image', "url('" + image_src + "')");
 
 
      });
      var keyword = 'mining'
     $.getJSON("http://api.flickr.com/services/feeds/photos_public.gne?jsoncallback=?",
     {
         tags: keyword,
         tagmode: "any",
         format: "json"
      },
      function(data) {
          console.log("function data");
          var rnd = Math.floor(Math.random() * data.items.length);
 
          var image_src = data.items[rnd]['media']['m'].replace("_m", "_b");
 
          $('.DistrictOtherMine').css('background-image', "url('" + image_src + "')");
 
 
      });
    });
    
    #CSS
    body {
    background-color: green;
}
#Districts{
    display: flex;
    justify-content: space-around;
    align-items: center; 
    font-family: arial;
    color: white;

}
.DistrictIpswitch {
    width: 400px;
    height: 400px;
    border: solid;
    border-color: black;
    border-width: 3px;
    background-size: 620px;
    background-repeat: no-repeat;

}
.DistrictIpswitch:hover{ 
    background-color: white;
}
.DistrictIpswitch > h1 {
    padding: 150px;

}
.DistrictIpswitch > h2 {
    padding: -30px;

}
.DistrictChartersTowers {
    width: 400px;
    height: 400px;
    border: solid;
    border-color: black;
    background-size: 620px;
    background-repeat: no-repeat;

}
.DistrictChartersTowers > h1 {
    padding: 150px;

}

.DistrictOtherMine {
    width: 400px;
    height: 400px;
    border: solid;
    border-color: black;
    background-size: 620px;
    background-repeat: no-repeat;

}
.DistrictOtherMine > h1 {
    padding: 150px;

}
.DistrictChartersTowers:hover{ 
    background-color: white;
}
a{
    text-decoration: none;
    color: white;
}
a:active {
    text-decoration: none;
    color: white;

}
