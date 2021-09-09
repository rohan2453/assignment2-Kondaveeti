Rohan Reddy Kondaveeti
i am from Telangana, India. I like the Places and the traditions and would like to go Trips with my friends. I like the winter season the most.

[myimage] https://github.com/rohan2453/assignment2-Kondaveeti/blob/main/image1.jpg


---------------------------------------------------------------------------------------------
Followinng is the list of food items and prices


| Food Item      | Location | Price    |
| :---        |    :----:   |          ---: |
| Pepsi    | kansas      |  $5   |
| Lemonade | maryville   |   $6    |
| sprite   | nashville   |   $7    |
| beer     | newyork     |   $8    |

-----------------------------------------------------------------------------------------

# Quotes

>Stick to journalism, Mr Cort, where you never have to understand anything.

  *- Iain Pears*

>Money is a tool, so I don't have to be.

  *― Eddie Mumford*

  ---------------------------------------------------------------------------------

  > String Hashing Algorithm
 
  [source] <https://en.wikipedia.org/wiki/Hash_function/>

  ```
vector<vector<int>> group_identical_strings(vector<string> const& s) {
    int n = s.size();
    vector<pair<long long, int>> hashes(n);
    for (int i = 0; i < n; i++)
        hashes[i] = {compute_hash(s[i]), i};

    sort(hashes.begin(), hashes.end());

    vector<vector<int>> groups;
    for (int i = 0; i < n; i++) {
        if (i == 0 || hashes[i].first != hashes[i-1].first)
            groups.emplace_back();
        groups.back().push_back(hashes[i].second);
    }
    return groups;
}
```

[source] <https://cp-algorithms.com/string/string-hashing.html>