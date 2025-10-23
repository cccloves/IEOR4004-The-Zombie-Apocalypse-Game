### IEOR4004: The Zombie Apocalypse Game

**Name:** Yihan Yu (yy3644)

Task: We need to leave the bunker and collect all the necessary supplies: One grocery store (two choices: Grocers1 or Grocery2), Pharmacy, Hospital, Gas Station.Finally, we should return to the bunker. The goal is to take the **shortest route** possible and avoid walking unnecessary paths.

##### Chosen Route

I calculated both options for the grocery store. The results are:Bunker → Grocers1 → Pharmacy → Hospital → GasStation → Bunker(2500), Bunker → GasStation → Pharmacy → Hospital → Grocery2 → Bunker(3100). So I chose **Grocers1**, because the total distance is shorter (2500 vs 3100).The Detailed Path:

```
Bunker → B → D → E → F → Grocers1 → F → J → Pharmacy → J → I → Hospital → I → GasStation → H → C → A → Bunker
```

This path is based on the **shortest paths on the actual road network**, so it avoids unnecessary backtracking and visits all required locations.

##### Strategy / How I Decided

I made a graph of the town with all nodes and roads. Then I calculated shortest distances between all pairs of important points. I used a **TSP solver with MTZ constraints** to find the shortest tour visiting all required points. I tested both grocery options and compared the total distance. The solver ensures that the tour is shortest among all possible sequences.

##### Map & Conclusion

<img src="/Users/yihanyu/Library/Application Support/typora-user-images/image-20251023142219220.png" alt="image-20251023142219220" style="zoom: 22%;" />

Code: Here is a link to my working code: https://github.com/cccloves/IEOR4004-The-Zombie-Apocalypse-Game

Conclusion: The route is efficient because it **minimizes total distance** while visiting all necessary points. Choosing **Grocers1** is the best way to collect all supplies and safely return to the bunker.
