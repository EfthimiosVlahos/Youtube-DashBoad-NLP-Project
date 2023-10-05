# YouTube Dashboard on Streamlit

<p align="center">  
    <br>
	<a href="#">
        <img height=100 src="https://cdn.svgporn.com/logos/youtube-icon.svg" hspace=20> 
	<img height=100 src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/1200px-Python-logo-notext.svg.png" hspace=20 >
        <img height=100 src="https://cdn.svgporn.com/logos/streamlit.svg" hspace=20> 
  	</a>	
</p>
<br>

Generating analytics based on a YouTube video and displaying key insights as a dashboard app hosted on Streamlit.

## Key Performance Indicators (KPI's)
For the dashboard, the following metrics are calculated:
- Total Number of Views
- Total Number of Likes
- Total Number of Comments
- Most Liked Comments 
- Comments in Different Languages on the video
- Most Replied Comments
- General Sentiment/Review Analysis

## Environment
- Python 3.10
- YouTube API
- Streamlit cloud

## Design
The data pipeline and design involve several steps:
- Create an API key with YouTube Data. Version 3 of the API was used for this project
- Extract the videoID from a given YouTube URL. This is usually the part that comes after the `v=` in the query string
- Using the API key, pull `snippet` and `statistics` from the YouTube API based on the video ID
- `Snippet` from `CommentThreads` contains many APIs. We focus mainly on Author, Comments, Timestamp, likes, and replies
- The `videos` API contains important `statistics` like viewCount, Likes, and Total Comments
- After processing all the required information, they are returned as dataframes
- These dataframes are used as the basis for various visualizations as displayed on the dashboard
- Using the capabilities and different components of Streamlit, we design the dashboard with KPI's

## Demo
[Check out the Live Demo Here!](https://youtube-dashboad-efthimiosvlahos-nlp-project-eqbg6nwmt2fwgjc8qu.streamlit.app/)

## Future Scope
- The YouTube API is limited to only 100 results per page. The workaround for this is to run a loop while processing the results from the first API request. Once this gets patched in the future, the analytics can be extended to show more NLP-based Sentimental analysis and more Language related analytics. This is because there would be more data points to go on beyond the initial 100.
- A time-series model/analytics can be displayed based on KPI's. For example:
  - Change of Likes over the last 30 days
  - Trend of viewership
  - Change in sentiments

## Contribution
Feel free to contribute to the enhancement of this project by creating a Pull Request.

## Acknowledgement
Thanks to all contributors and to YouTube and Streamlit for providing the API and the platform respectively.

