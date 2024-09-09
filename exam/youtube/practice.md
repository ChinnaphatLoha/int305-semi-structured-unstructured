# XPath Query Problems

## Basic Queries

**1.** Find all video titles.

- _Expected Result_: List of titles for all video nodes.

**2.** Find the description of all playlists.

- _Expected Result_: List of descriptions for all playlist nodes.

**3.** Retrieve all video view counts.

- _Expected Result_: List of view counts for all video nodes.

**4.** List all tags used in the playlists.

- _Expected Result_: List of all tag nodes within tags elements.

**5.** Find all playlist titles.

- _Expected Result_: List of titles for all playlist nodes.

## Intermediate Queries

**6.** Find all videos in the playlist titled "Top 10 Music Hits".

- _Expected Result_: List of video nodes under the playlist with title "Top 10 Music Hits".

**7.** Find all videos uploaded after "2024-01-01".

- _Expected Result_: List of video nodes with upload dates after "2024-01-01".

**8.** Retrieve all videos where the category is "Education".

- _Expected Result_: List of video nodes under playlists categorized as "Education".

**9.** Find all playlists that contain the tag "DailyLife".

- _Expected Result_: List of playlist nodes that include the tag "DailyLife".

**10.** Get the view count of videos in the playlist titled "Daily Vlog Adventures".

- _Expected Result_: List of view counts for videos in the playlist with title "Daily Vlog Adventures".

## Advanced Queries

**11.** Find all videos where the view count is greater than 50,000.

- _Expected Result_: List of video nodes where view count exceeds 50,000.

**12.** Retrieve titles of videos with more than 1,000 likes.

- _Expected Result_: List of titles for videos with more than 1,000 likes.

**13.** Find playlists with more than 1 video.

- _Expected Result_: List of playlist nodes containing more than 1 video.

**14.** Get the titles of all videos in playlists categorized under "Music" or "Gaming".

- _Expected Result_: List of titles for videos in playlists categorized as "Music" or "Gaming".

**15.** List all video titles where the duration is longer than 10 minutes.

- _Expected Result_: List of titles for videos with a duration longer than 10 minutes.

**16.** Find all video titles where the title contains "Epic" (using `contains()`).

- _Expected Result_: List of titles for videos containing "Epic".

**17.** Find the maximum number of likes for videos in the playlist titled "Top 10 Music Hits" (using `max()`).

- _Expected Result_: Maximum value of likes for videos in the "Top 10 Music Hits" playlist.

**18.** Retrieve the average view count of all videos (using `avg()`).

- _Expected Result_: Average value of view counts for all videos.

**19.** Find all distinct tags used in playlists (using `distinct-values()`).

- _Expected Result_: List of unique tag values used across playlists.

**20.** Get the duration of the last video in the playlist titled "Daily Vlog Adventures" (using `last()`).

- _Expected Result_: Duration of the last video in the "Daily Vlog Adventures" playlist.
