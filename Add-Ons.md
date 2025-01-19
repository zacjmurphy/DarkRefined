# 🧩 Add-on:  Custom media covers for ElegantFin
This is a Jellyfin add-on that allows you to customise My Media cover arts. This is an experimental feature, so limited support will be provided.

#### **Author:** [lscambo13](https://github.com/lscambo13)

<hr>

### 👇 How to enable this add-on? 

- Paste the following at the end in Custom CSS code box:

```
@import url("https://cdn.jsdelivr.net/gh/lscambo13/ElegantFin@main/Theme/assets/add-ons/custom-media-covers-nightly-min.css");
```

<hr>

### ⚙️ How to modify this add-on? 

- To configure your theme to use the custom images, you'll need to input a URL pointing to an image in variables starting with '--url' and an overlay color in variables starting with '--color'.
	
- The ideal Jellyfin cover sizes are `960px x 540px`, and the colors should be in rgb format i.e. `rbg(128, 128, 128)`.
  
- Below are all the configurable variables, but you should remove the entries you do not intend to modify:


```
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
```

### 🆗 Read this example:
Suppose you want to modify the Live TV cover art. You'll have to modify the variables named `--colorOverlayLivetvCover` and `--urlLivetvCover`, so that your final configuration will look something like this:

```
@import url("https://cdn.jsdelivr.net/gh/lscambo13/ElegantFin@main/Theme/assets/add-ons/custom-media-covers-nightly-min.css");

:root{
    --colorOverlayLivetvCover: rgb(39, 68, 185);
    --urlLivetvCover: url(https://artworks.thetvdb.com/banners/fanart/original/71663-33.jpg);
}

```

<hr>

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

