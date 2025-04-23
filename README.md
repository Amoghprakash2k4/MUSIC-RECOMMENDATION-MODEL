# HetRec2011 Last.fm 2K Dataset

## Version
**1.0** (Released May 2011)

## Description
The **HetRec2011 Last.fm 2K Dataset** contains social networking, tagging, and music artist listening information from 1,892 users on the Last.fm online music platform.

This dataset was released as part of the **2nd International Workshop on Information Heterogeneity and Fusion in Recommender Systems (HetRec 2011)**, co-located with the **5th ACM Conference on Recommender Systems (RecSys 2011)**.

- Last.fm: [http://www.last.fm](http://www.last.fm)  
- HetRec 2011: [http://ir.ii.uam.es/hetrec2011](http://ir.ii.uam.es/hetrec2011)  
- RecSys 2011: [http://recsys.acm.org/2011](http://recsys.acm.org/2011)

## Data Statistics

- **Users:** 1,892  
- **Artists:** 17,632  
- **User Friend Relations:** 12,717 bi-directional (25,434 pairs)  
  - Avg. 13.443 friends per user  
- **User-Artist Listen Events:** 92,834  
  - Avg. 49.067 artists per user  
  - Avg. 5.265 users per artist  
- **Tags:** 11,946  
- **Tag Assignments:** 186,479  
  - Avg. 98.562 tags per user  
  - Avg. 14.891 tags per artist  
  - Avg. 18.930 distinct tags per user  
  - Avg. 8.764 distinct tags per artist

## Files

### `artists.dat`
- Information about music artists.
- Format:  
  ```
  artistID \t name \t url \t pictureURL
  ```
- Example:  
  ```
  707	Metallica	http://www.last.fm/music/Metallica	http://userserve-ak.last.fm/serve/252/7560709.jpg
  ```

### `tags.dat`
- Contains available tags.
- Format:  
  ```
  tagID \t tagValue
  ```
- Example:  
  ```
  1	metal
  ```

### `user_artists.dat`
- Artists listened to by each user, along with listen count (weight).
- Format:  
  ```
  userID \t artistID \t weight
  ```
- Example:  
  ```
  2	51	13883
  ```

### `user_taggedartists.dat`
- Tag assignments (with date) made by users for artists.
- Format:  
  ```
  userID \t artistID \t tagID \t day \t month \t year
  ```
- Example:  
  ```
  2	52	13	1	4	2009
  ```

### `user_taggedartists-timestamps.dat`
- Same as `user_taggedartists.dat`, but with Unix timestamp instead of date.
- Format:  
  ```
  userID \t artistID \t tagID \t timestamp
  ```
- Example:  
  ```
  2	52	13	1238536800000
  ```

### `user_friends.dat`
- Social network: user friendships.
- Format:  
  ```
  userID \t friendID
  ```
- Example:  
  ```
  2	275
  ```

## License
Please refer to the HetRec 2011 dataset usage policy and terms provided by the workshop or the original dataset website.
