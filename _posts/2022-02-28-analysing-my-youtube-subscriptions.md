---
title: Analysing my YouTube subscriptions & views over the last 4 years (and how you can too!)
image: /assets/images/2022/youtubetypes.png
tags:
    - Google
    - YouTube
    - Calculations
    - Data
---

According to Wallace Boyer in [Chuck Palahniuk's "Rant"](https://www.goodreads.com/book/show/22285.Rant): "... every person is obsessed with himself. You are your own favorite hobby. You're an expert on you". With that in mind, I spent some time exploring my YouTube viewing / subscribing habits over the last few years! 

Yes, this post is going to be of limited interest to anyone besides myself / any stalkers I happen to have. However, detailing the simple steps I took may help you to do the same!

You can also just [view my final spreadsheet](https://docs.google.com/spreadsheets/d/1LJBg9aZL42ri1tEoPPzrRX4M2Q_podGX2CDbGC4OCpk/edit).

## Preparing the spreadsheet

### Google Takeout

For a few years, Google have had an excellent [Takeout](https://takeout.google.com/settings/takeout) service available, where you can export data on demand. 

To save time, just select "YouTube and YouTube Music" with the "history" and "subscriptions" options:

[![](/assets/images/2022/youtubetypes-thumbnail.png)](/assets/images/2022/youtubetypes.png)

After requesting the takeout, you should receive an email in 5-10 minutes with a link to download your export:

[![](/assets/images/2022/youtubeemail-thumbnail.png)](/assets/images/2022/youtubeemail.png)

### Creating the spreadsheet

Inside your takeout zip file, you'll find `/history/watch-history.html`, a list of every video you've watched! As a heavy YouTube user this only showed the last 4 years, but it may show much further back for you.

You'll also find `/subscriptions/subscriptions.csv`, a list of all your current subscriptions (ID, URL, name).

If you open up Google Sheets, you can import your subscriptions to start analysing the data via `File` -> `Import`:

[![](/assets/images/2022/youtubeimport.png)](/assets/images/2022/youtubeimport.png)

### Adding view counts

Now we have a basic spreadsheet, I wanted to know how many times I'd watched a video from each YouTuber. This could have been done programmatically, but doing it manually was quick enough.

There are 2 ways to get this count, both easy but repetitive:
1. Open the `watch-history.html` file in your browser (it might take a while to load!), and simply search for each YouTuber's username (Ctrl + F). 10 results = 10 views.
2. Open the `watch-history.html` in a decent text editor like VS Code or Notepad++. Search for each YouTuber's ID for a guaranteed accurate count of videos watched.

There's nothing clever or complicated involved, just repeating a 2-3 second action a couple of hundred times!

### Adding subscriber count & genre

I next decided I wanted to know what genres I watched, and how popular the channels were. For subscriber count, I just opened each URL and wrote down the subscriber count. After doing it a few times, it'll become very quick & automatic!

For genre I decided to use my own categories, as YouTube's are quite broad (e.g. "Gaming"). I defined these in a new sheet "Genres", and added data validation to the whole "Genre" column in my main sheet (right click -> more actions -> data validation):

[![](/assets/images/2022/youtubegenre-thumbnail.png)](/assets/images/2022/youtubegenre.png)

### "Fan factor"

Finally, I wanted some sort of measurement of the "nicheness" of a channel. For example, which relatively unknown channels have I watched many videos from, and vice versa. To approximate these, I just used `videos watched / channel's subscribers`, then x100 to make the numbers easier to work with:

[![](/assets/images/2022/youtubefanfactor-thumbnail.png)](/assets/images/2022/youtubefanfactor.png)

I then used `LARGE` for the first time, which gets the Xth biggest number in a range, to find my highest and lowest fan factors. The formula for the highest fan factor was `=LARGE('Raw data'!G$2:G$398, 1)`.

## Viewing the spreadsheet

The [spreadsheet itself is here](https://docs.google.com/spreadsheets/d/1LJBg9aZL42ri1tEoPPzrRX4M2Q_podGX2CDbGC4OCpk/edit), if you'd like to see the formulas etc.

### Most viewed channels

I was actually pretty surprised by the final results of this! My top channels over the past 4 years:

Channel title          |Channel subs|Channel genre       |Videos watched|"Fan factor"
-----------------------|------------|--------------------|--------------|------------
[penguinz0](http://www.youtube.com/channel/UCq6VFHwMzcMXbuKyG7SQYIg) |10,100,000  |Gaming - Cr1tikal   |1514          |0.01499     
[Hat Films](http://www.youtube.com/channel/UC7A_dLnSAjl7uROCdoNyjzg) |890,000     |Gaming - Yogscast   |1178          |0.13236     
[Twitch Clips - Jerma985](http://www.youtube.com/channel/UCN4LK4QnhUdhvSGSu40Tf4A) |64,900      |Gaming - Jerma985   |1162          |1.79045     
[YOGSCAST Lewis & Simon](http://www.youtube.com/channel/UCH-_hzb2ILSCo9ftVSnrCIQ) |7,140,000   |Gaming - Yogscast   |1040          |0.01457     
[FailRace](http://www.youtube.com/channel/UCtf9LFKV46qxZifbrPd91vQ) |507,000     |Gaming - Racing     |933           |0.18402     
[JakeandAmir](http://www.youtube.com/channel/UCNNxmRzlheZAeZuMYakh6vQ) |67,300      |Comedy              |850           |1.26300     
[2ndJerma](http://www.youtube.com/channel/UCL7DDQWP6x7wy0O6L5ZIgxg) |577,000     |Gaming - Jerma985   |845           |0.14645     
[Angory Tom](http://www.youtube.com/channel/UC5rUMdCFWPXYs9e8PBLzq5g) |248,000     |Gaming - Yogscast   |795           |0.32056     
[Hat Gaming](http://www.youtube.com/channel/UCJYvnogbZIQQvX9exn5aDPw) |149,000     |Gaming - Yogscast   |598           |0.40134     
[Duncan](http://www.youtube.com/channel/UCs4br3aZLU0sOEM-3n0-6xQ) |1,740,000   |Gaming - Yogscast   |463           |0.02661     
[fantano](http://www.youtube.com/channel/UCnxQ8o9RpqxGF2oLHcCn9VQ) |1,440,000   |Music - Review      |368           |0.02556     
[LockPickingLawyer](http://www.youtube.com/channel/UCm9K6rby98W8JigLoZOh6FQ) |3,830,000   |Hobbies             |356           |0.00930     
[3kliksphilip](http://www.youtube.com/channel/UCmu9PVIZBk-ZCi-Sk2F2utA) |1,020,000   |Gaming - Valve Games|351           |0.03441     
[Yogscast Live](http://www.youtube.com/channel/UCQBs359lwzyVFtc22LzLjuw) |262,000     |Gaming - Yogscast   |350           |0.13359     
[Jerma Stream Archive](http://www.youtube.com/channel/UC2oWuUSd3t3t5O3Vxp4lgAA) |136,000     |Gaming - Jerma985   |343           |0.25221     

Turns out, if you combine Hat Films & Hat Gaming, they're my most watched creators (excluding clip channels)! It's a bit of a surprise, since I don't feel like they put out TONS of videos. However, consistent high quality (and a rewatchable back catalog) apparently pays off. Excluding the spin-off / reupload channels, Angory Tom is the lowest subscribed (i.e. most underrated) creator in the top 15.

I often put on YouTube reuploads of old Twitch streams when I can't sleep, so I thought channels like Jerma Stream Archive would be high. However, since the streams are 4-5hr long, there'd only be 2 views even if I watched all night! Contrastingly Jake and Amir have hundreds of 2-5 minute videos, so hundreds of views can be amassed in just a couple of hours total.

It's not very surprising that most of my top YouTubers are gaming based, since I often have gaming videos in the background whilst working, like TV. I'm surprised 3kliksphilip is there, since he has his views split between 3 channels, and uploads less frequently than other YouTubers. The high view count despite this probably reflects the consistently high quality and attention to detail in his videos.

## Genres

Unsurprisingly, when grouped by genre gaming videos make up the vast majority of my viewing:

Genre                  |\# Channels|\# Views
-----------------------|-----------|--------
Gaming - Yogscast      |44         |6532    
Gaming - Jerma985      |25         |3274    
Gaming - Runescape     |37         |2799    
Gaming - Cr1tikal      |4          |1955    
Music - Artists        |44         |1777    
Comedy                 |20         |1633    
IRL                    |10         |1593    
Infotainment - IRL     |36         |1461    
Gaming - Racing        |11         |1263    
Music - Review         |8          |939     
Gaming - Valve Games   |13         |832     
Gaming - Misc          |30         |781     
Technology - Space     |14         |687     
Hobbies                |13         |637     
Infotainment - Internet|13         |526     
Gaming - Speedrunning  |11         |396     
Technology - Hardware  |13         |319     
Animals                |7          |228     
Film / TV Review       |8          |209     
Gaming - Game Dev      |11         |188     
Technology - Cars      |10         |183     
Infotainment - Crime   |9          |108     
Technology - Software  |5          |34      
Other                  |1          |26      

My interests in space, cars, and car games have really ramped up in the last 2-3 years, so I expect the top 2-3 genres reflect 2018-19 more than 2020-2022. It's also amazing that I'm subscribed to 25 Jerma channels, when there are only 2 official ones! The community has a *lot* of fan-made content.

That single "Other" channel is [LOCAL58TV](https://www.youtube.com/c/LOCAL58TV) which... really doesn't fit in any category. 

## Best and worst "Fan factor"

I was hoping my "fan factor" calculation (my views / channel subs) would highlight some great small creators that I really enjoy. Unfortunately, it highlighted... tiny channels that have made 1-2 spin-off videos (e.g. a Jerma985 compilation), some personal friends and not much else. A future improvement would be perhaps filtering out channels with < 5 videos and < 1000 subs.

The low "fan factor" is unsurprisingly channels that I don't actually watch videos from. In this case it's a large YouTuber, 3 musicians, and a great channel that has stopped uploading:

Rank|Fan Factor|Channel                  
----|----------|-------------------------
1   |42.85714  |[Trotts Bulge](http://www.youtube.com/channel/UCMe-8NXf9h50WTzP2z7LCHA)           
2   |21.27660  |[Biggles OutbreakCommunity](http://www.youtube.com/channel/UCg0MHTlF4cuvuW03TrJLyqA)
3   |15.15152  |[Lewiiiiiiiis](http://www.youtube.com/channel/UCQ5WORSXJqJQS0a3XUyafDg)         
4   |12.50000  |[Gunlexify](http://www.youtube.com/channel/UCQv84wrJ9BRC6zVtynz0dvg)             
5   |5.87515   |[BeastlyHaz](http://www.youtube.com/channel/UCaot2Q18NsddbNva4PzmorQ)        
... |          |                         
393 |0.00008   |[Ice Cube / Cubevision](http://www.youtube.com/channel/UCRZvImLvRIE5BoZvmVHMTqw)
394 |0.00007   |[brusspup](https://www.youtube.com/user/brusspup)
395 |0.00004   |[The Game](http://www.youtube.com/channel/UC3eKKASjWY-WAGRII9iKHsQ)          
396 |0.00002   |[colinfurze](http://www.youtube.com/channel/UCp68_FLety0O-n9QU6phsgw)      
397 |0.00002   |[Drake](http://www.youtube.com/channel/UCByOQJjav0CUDwxCk-jVNRQ)

## Summary

So, what did I learn? Well, I learned that I like YouTubers with consistently high quality gaming videos, which I probably already knew! I also found that I've watched at least 1 video from all of my subscriptions in the last 4 years, even those that haven't uploaded in 5-6 years. Some of them could probably be removed though, if I've only watched a single video!

Was it worth the time taken? I learnt a few things about Google Sheets, and it was an interesting diversion, so *yes*. Just.