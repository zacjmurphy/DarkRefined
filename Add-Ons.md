# Add-on:  Custom media covers for ElegantFin
This is a Jellyfin add-on that allows you to customise My Media cover arts. This is an experimental feature.


#### **Author:** [lscambo13](https://github.com/lscambo13)

<hr>


### 🖼️ Previews

<details>
  <summary><i>Click here to reveal</i></summary>
  
<img src="https://github.com/lscambo13/ElegantFin/blob/main/Previews/1.%20Homepage.png" style="width:360px;height:auto;"></img>

</details>

<hr>

### 👇 How to setup this theme? 

<b>
- To configure your theme to use the custom images, you'll need to input a URL pointing to an image in variables starting with '--url' and an overlay color in variables starting with '--color'.
- Default Jellyfin cover sizes are 960px x 540px.
- The colors should be in rgb format i.e. rbg(128, 128, 128).
- You should remove the entries you do not intend to modify.
- paste the following at the end in Custom CSS code box after making the necessary changes:</b>

'''

	@import url("");

  :root{

    <!-- overlay colors; change according to your image. -->
    --colorOverlayMoviesCover: rgb();
    --colorOverlayTvshowsCover: rgb();
    --colorOverlayLivetvCover: rgb();
    --colorOverlayPlaylistsCover: rgb();
    --colorOverlayBoxsetsCover: rgb();
    --colorOverlayMusicCover: rgb();
    --colorOverlayHomevideosCover: rgb();
    --colorOverlayBooksCover: rgb();
    --colorOverlayFoldersCover: rgb();

    <!-- cover images; input the url pointing to an image. -->
    --urlMoviesCover: url();
    --urlTvshowsCover: url();
    --urlLivetvCover: url();
    --urlBoxsetsCover: url();
    --urlMusicCover: url();
    --urlHomevideosCover: url();
    --urlBooksCover: url();
    --urlFoldersCover: url();
}

'''

Suppose you want to modify the Live TV cover art. You'll have to modify the variables --colorOverlayLivetvCover and --urlLivetvCover, so that your configuration will look something like this:
'
	@import url("");

  :root{
    --colorOverlayLivetvCover: rgb(39, 68, 185);
    --urlLivetvCover: url(https://artworks.thetvdb.com/banners/fanart/original/71663-33.jpg);
}

'
<details>
  <summary><i>Detailed steps for server-side implementation</i></summary>

1. Open Dashboard from Administration tab in Settings.
2. Select General tab from the side bar.
3. Scroll down to find Custom CSS code box under Branding section.
4. Paste the custom css in Custom CSS code box.
5. Click save
</details>

<details>
  <summary><i>Detailed steps for client-side implementation</i></summary>

1. Open Display tab in Settings.
2. Scroll down to find Custom CSS code box.
3. Paste the custom css in Custom CSS code box.
4. Click save.
</details>


<hr>

