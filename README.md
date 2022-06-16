# 20,000 Boardgames Data Analysis

<!-- wp:buttons -->
<div class="wp-block-buttons"><!-- wp:button -->
<div class="wp-block-button"><a class="wp-block-button__link" href="https://www.linkedin.com/in/suhita-acharya/" target="_blank" rel="noreferrer noopener">LinkedIn</a></div>
<!-- /wp:button -->

## Introduction

<!-- wp:paragraph -->
<p>As the pandemic hit everywhere and as the lockdowns were imposed, we saw more people spending their time at home and with family and friends in their bubble. This practice became more prevalent during the winter months when safe outdoor socializing was no longer possible. To break the monotony of stay-at-home life, people turned to much-loved pass time of playing boardgames.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>A Today.com <a href="https://www.today.com/popculture/board-games-enjoy-surge-popularity-during-pandemic-t202377" target="_blank" rel="noreferrer noopener" title="article">article</a> reporting on the boardgame surge in popularity stated that Hasbro, a popular game-making company had reported a 20% growth in sales in the third quarter of 2020 compared to 2019 at the same time, and similarly Mattel, another game-maker showed that game sales were up 48% in 2020. People started looking at sites, myself included, such as <a href="https://boardgamegeek.com/" target="_blank" rel="noreferrer noopener" title="Board Game Geek">Board Game Geek</a> (BGG) to look at some of the top board games and their ratings before deciding on which games to buy. This site also includes a page with a list of the top 100 board games ranked based on their Geek Rating.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Question of Interest</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>From a preliminary BGG site review, it can be deduced that a board game’s user ratings on any online platform can be analogous to its overall popularity. For this project, I decided to research whether certain metrics on an online board game database platform contribute to a board game's rating/popularity. I decided to use a dataset from Kaggle - <a href="https://www.kaggle.com/datasets/extralime/20000-boardgames-dataset" target="_blank" rel="noreferrer noopener" title="20,000 Boardgames Dataset">20,000 Boardgames Dataset</a> that used data for 20,000 boardgames directly scraped from the BGG site.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>This project compares BGG Geek Rating to different metrics to see if they influence the game’s rating in any way. This project aims to aid Game Developers trying to increase their game’s low user rating/popularity and eventually increase sales for the game or those developing a new game and looking to research the best metrics to incorporate in order to maximize future game ratings.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Dataset Introduction</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Before we begin, let us discuss what the BGG site's Geek Rating is. As per a <a href="https://tbgd.blog/2019/01/25/guide-to-boardgamegeek/" title="blog">blog</a> from the site The Board Game Detective, Geek Rating is a value that is computed using the User Ratings as input but with some alterations. BGG site mentions that this rating prevents games with relatively few votes from climbing to the top of the BGG Ranks, and artificial "dummy" votes are added to the User Ratings to come up with these ratings.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The dataset that I used, contains a vast amount of information for several board games including their ranks and rating such as their genre, the year the game was published, game playing time, minimum payer age, name and counts of developers/designers, social media blog, podcast, article counts, etc. Some features that I was interested in for this project were as follows:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Site views for games on the BGG site.</li><li>The total number of awards won by the game.</li><li>Mentions of the game in different media types such as news/online review articles, blog posts, and podcasts.</li><li>Different categories/genres of the game.</li><li>Minimum and maximum playing time for the game.</li></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2>Geek Rating Evaluation</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>When I conducted a geek rating evaluation for all the games, I discovered that most of the games lie between the rating range of 5 through 7. Also, from the histogram below we can see that the geek rating category >5 and &lt;6 has the highest number of games among all other categories.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":85282,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img2-586705-u0cNOR5K.png" alt="" class="wp-image-85282"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Similarly, if we look at the top and bottom 150 games sorted by their geek rating, we can see that most of the top 150 highest-rated games lie between the 7 through 9 range. Also, most of the 150 lowest-rated games lie between the 3.5 through 5.5 range.</p>
<!-- /wp:paragraph -->

<!-- wp:gallery {"linkTo":"none"} -->
<figure class="wp-block-gallery has-nested-images columns-default is-cropped"><!-- wp:image {"id":85365,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/rec1-207741-lNdeaDOq.png" alt="" class="wp-image-85365"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":85364,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/rec2-383707-nWiBJ7vl.png" alt="" class="wp-image-85364"/></figure>
<!-- /wp:image --><figcaption class="blocks-gallery-caption"><strong>Ratings histogram for boardgames - 150 highest and lowest rated games </strong></figcaption></figure>
<!-- /wp:gallery -->

<!-- wp:heading -->
<h2>Site Views Evaluation</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Next in this research, I looked at the relationship between site views (views for the board game on the BGG site) and geek ratings for different board games. When I studied the number of site views (in millions) and geek rating, it became obvious that for the top 150 highest-rated games, as the site views increased the game's rating increased as well.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The same could not be said however for the 150 lowest-rated games (for the purpose of this project only games with rating > 0 were included). For these games, the site views generally stayed below 1 million regardless of what the geek rating was. Overall, from all 20,000 games, in the games with ratings > 6.5 a trend of rising in rating with increased site views was seen.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":85298,"sizeSlug":"full","linkDestination":"none"} -->
<figure class="wp-block-image size-full"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img7-348289-4Q5QAnGd.png" alt="" class="wp-image-85298"/></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>Game Awards Evaluation</h2>
<!-- /wp:heading -->

<!-- wp:image {"id":85303,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img8-052847-Jl0iz8DV-1024x496.png" alt="" class="wp-image-85303"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>In this project, the next thing I wanted to review was the number of awards top and bottom 20 rated games have received. For this study, I looked at 20 highest-rated games and 20 lowest-rated games after excluding games that had a rating of 0 and the games which had received at least one award. What I uncovered was that the top-rated games had received more awards (some games had received upwards of 20 awards), while the bottom-rated games received only one or two awards between them.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":85304,"width":843,"height":417,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large is-resized"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img9-519500-RoLlx65R-1024x508.png" alt="" class="wp-image-85304" width="843" height="417"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>What I also found out was that if we look at the average award counts per geek rating category, the highest rating category also had a high average awards count (greater than all other categories).</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":85306,"sizeSlug":"full","linkDestination":"none"} -->
<figure class="wp-block-image size-full"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img10-763932-rIGQnC0b.png" alt="" class="wp-image-85306"/></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>Media Exposure Evaluation</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>For the next evaluation, the feature of interest will be compared with site views as higher site views can translate to higher ratings. From the graph and the table listed below, it looks like higher rating categories have high median site views.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":85395,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img1-177353-78mhKMv7-1024x582.png" alt="" class="wp-image-85395"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>For this next evaluation, I looked at whether there was a relationship between the count of game-related media content and a game's geek ratings. The media types that were looked at were:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Podcasts: External game-related podcasts</li><li>Weblinks: External game-related media/content</li><li>BGG News articles</li><li>BGG Blog posts</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>For this evaluation, games with geek rating greater than 0, site views less than 6 million, and having least one game-related media content were looked at.</p>
<!-- /wp:paragraph -->

<!-- wp:gallery {"linkTo":"none"} -->
<figure class="wp-block-gallery has-nested-images columns-default is-cropped"><!-- wp:image {"id":85368,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img2-391616-ihwFMFG1.png" alt="" class="wp-image-85368"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":85367,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img3-729084-9F9VFKSI.png" alt="" class="wp-image-85367"/></figure>
<!-- /wp:image --><figcaption class="blocks-gallery-caption"><strong>Site Views vs. Podcasts/Weblink count scatterplots</strong></figcaption></figure>
<!-- /wp:gallery -->

<!-- wp:paragraph -->
<p>From the above graphs, we can see that there is a definite trend between the number of podcasts and web links mentioning the game and the site views for the game on its page on the BGG site. Generally, the higher the number of articles written higher the site views were found to be. The same could be said true for blogs written by the BGG site; however, not for the news articles written by BGG.</p>
<!-- /wp:paragraph -->

<!-- wp:gallery {"linkTo":"none"} -->
<figure class="wp-block-gallery has-nested-images columns-default is-cropped"><!-- wp:image {"id":85369,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img4-796260-TZImQA58.png" alt="" class="wp-image-85369"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":85370,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img5-548431-VhT802wd-1024x772.png" alt="" class="wp-image-85370"/></figure>
<!-- /wp:image --><figcaption class="blocks-gallery-caption"><strong>Site Views vs. BGG News Articles/Blog Posts count scatterplots</strong></figcaption></figure>
<!-- /wp:gallery -->

<!-- wp:heading -->
<h2>Game Genre vs. Rating Evaluation</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>I also studied the game genres having highest average geek rating in each of the rating categories and found out that some game genres such as Adventure, Medieval, City Building, Exploration, Miniatures and Civilization are more common in the games in top two higher rating categories.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":85343,"width":852,"height":356,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large is-resized"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img6-387743-KNiI6aVw-1024x428.png" alt="" class="wp-image-85343" width="852" height="356"/><figcaption><strong>Game categories with top rated genres and count of games that contributed to that average</strong></figcaption></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>Maximum and Minimum playing time per rating category</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>For the last evaluation, I looked at minimum and maximum playing time for the top two highest-rated categories. What we notice here is that the minimum paying time for each category lies between 30 minutes to 60 minutes for most of the games and the maximum playing time lies in a broader range of 30 min to 120 minutes.</p>
<!-- /wp:paragraph -->

<!-- wp:gallery {"linkTo":"none"} -->
<figure class="wp-block-gallery has-nested-images columns-default is-cropped"><!-- wp:image {"id":85377,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img7-348390-g9L7AvAM-1024x389.png" alt="" class="wp-image-85377"/></figure>
<!-- /wp:image --></figure>
<!-- /wp:gallery -->

<!-- wp:gallery {"linkTo":"none"} -->
<figure class="wp-block-gallery has-nested-images columns-default is-cropped"><!-- wp:image {"id":85374,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2022/06/suhita-acharya/img8-984593-1llRINaN-1024x420.png" alt="" class="wp-image-85374"/></figure>
<!-- /wp:image --></figure>
<!-- /wp:gallery -->

<!-- wp:heading -->
<h2>Takeaways/Conclusions</h2>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>Game developers can work towards getting their game more exposure on gaming database sites. Higher game site views could translate to higher ratings for the game.</li><li>Developers can promote awards the game has won on game sites so potential customers can read about it, gauge quality and competency, rate the game accordingly and make sales-related decisions based on it.</li><li>Quality game-related media content (especially blogposts and podcasts) on the site can boost viewability, possibly game rating, and eventually sales.</li><li>More publicity and media coverage a game would get, the more popular it would be which may in turn drive up sales.</li><li>New game developers can focus on developing games with certain genres listed below for a rating boost:<ol><li>Adventure</li><li>Medieval</li><li>City Building</li><li>Miniatures</li><li>Civilization</li><li>Exploration</li></ol></li><li>New game developers can focus on using a certain minimum or maximum game playing time (recommendations listed below) for future game rating positive impact.<ol><li>Minimum playing time: 30 min to 60 min.</li><li>Maximum playing time: at least 30 min and no more than 120 min.</li></ol></li></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2>Future Work</h2>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>Evaluation of data from other gaming database platforms to compare findings.</li><li>To evaluate whether a game’s rating influences its price and sales.</li><li>Further research for rated games, to see the number of times consumers click on game sales links on database platforms (if available) to demonstrate an interest in the game.</li></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2>References:</h2>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>Weisholtz, D., 2020. <em>How classic board games are bringing families closer during the pandemic</em>. [online] TODAY.com. Available at: &lt;https://www.today.com/popculture/board-games-enjoy-surge-popularity-during-pandemic-t202377> [Accessed 14 June 2022].</li><li>Boardgamegeek.com. n.d. <em>BoardGameGeek</em>. [online] Available at: &lt;https://boardgamegeek.com/> [Accessed 14 June 2022].</li><li>Kaggle.com. 2020. <em>20,000 Boardgames Dataset</em>. [online] Available at: &lt;https://www.kaggle.com/datasets/extralime/20000-boardgames-dataset> [Accessed 15 June 2022].</li><li>The Boardgame Detective. 2019. <em>Guide to BoardGameGeek Weightings and Ratings, and How to Find Good Games</em>. [online] Available at: &lt;https://tbgd.blog/2019/01/25/guide-to-boardgamegeek/> [Accessed 15 June 2022].</li></ul>
<!-- /wp:list -->  
