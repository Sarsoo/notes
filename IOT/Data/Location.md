---
onenote-id: 0-5264d661e55d455087663db7a52dca90!1-D084F068F621FF9!3928
---
Location Data
 
- Lat/Long
	- Can’t Euclidean distance
 ![Latitude North South POON 4 00 450S goos Latitude ...](../../../../../img/OneNote/Location%20image%2031d71e638e9b50d6.png)  

GeoHashing
 
- Encode lat/lon pairs
	- Geo-coding
- Hierarchical structure
- Interleaving lat/lon bits
- Use Base-32 char map
	- 5 bits per character
- Different sized segments
	- Fixed spatial bounding box
	- More characters = more precise
- Check closeness by seeing how long matching prefix is
	- Doesn't work if straddle a break point
- Close to north and south pole can have wildly different codes
- Bounding box
	- Better proximity searches by using surrounding 8 hashes
		- More complex

![5 1.236127 0.574036 Guildford gcpe6zmbpfrd 51.2431...](../../../../../img/OneNote/Location%20image%20b520fe2766271e63.png) ![Location Geohash location tag gcped86y1 mzg gcped8...](../../../../../img/OneNote/Location%20image%200b99a06012be5e1d.png)

![Minlong 0.6 miles 37.7545186015625. 122.4206 54296...](../../../../../img/OneNote/Location%20image%20b5acda1473846b05.png)

- Location codes

![Machine generated alternative text The naversine f...](../../../../../img/OneNote/Location%20image%2067d1dd329b7cc86a.png) ![Machine generated alternative text Haversine formu...](../../../../../img/OneNote/Location%20image%205fa160eb62d22e7e.png)