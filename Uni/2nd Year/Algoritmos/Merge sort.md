#todo explain merge sort
>[!tldr] 
>As the first step we keep splitting our data in half until sorting each half is trivial (aka our half length is either 2 or 1)
>We sort those halves
>We then start merging adjacent halves together. This is simplified by the fact that our halves are now sorted. We can use that to our advantage by selecting the maximum of our halves ($O(1)$ operation) and picking between the biggest. We then insert that into our new 2 halves array.
