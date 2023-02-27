# Lab Report 3: Researching Commands
## Choose of Commands: `prep`
1. `-v` : This option stands for "invert match," and it tells `grep` to only display lines that do not match the specified pattern.
2. `-r` : This option stands for "recursive," and it tells `grep` to search through all files and directories in the specified directory (or directories).
3. `-i` : This option stands for "ignore case," and it tells `grep` to perform a case-insensitive search.
4. `-c` : This option stands for "count," and it tells `grep` to display only the number of lines that match the specified pattern.
## Examples and Breakdowns
### For `-v`:

**Example 1 Input:**
```
grep -v "the" written_2/travel_guides/berlitz2/California-History.txt
```
**Example 1 Output:**
```
A Brief History
The Spanish Missions
The Mexicans
The American Pioneers
The Gold Rush
Statehood
The Great Earthquake
Reform, Progress, and Oil
Hollywood
Depression and Boom

Beatniks, Hippies, and Modern Times
```
**Example 1 Comment:** This option prompts an output to show all lines in the file `California-History.txt` that doesn't contain the keyword `"the"`. It's useful when we wanna find lines that don't contain a certain keyword.

**Example 2 Input:**
```
grep -v "^[[:space:]]*$" written_2/travel_guides/berlitz2/California-History.txt
```
**Example 2 Output:**
```
A Brief History
The first wave of California immigrants arrived somewhere between 20,000 and 35,000 years ago — wandering Asiatic tribes who entered the American continent via the Bering Strait, which at that time was dry land, or perhaps covered in ice. In the succeeding centuries, their descendants continued to push south and east, and eventually spread out to people the whole of the continent from Alaska to Patagonia. The tribes who decided to settle in what is now California were fortunate in their choice of homeland. The climate was very pleasant, and food was sufficiently plentiful for them to avoid the constant warfare that plagued many tribes elsewhere in the Americas.
```
...
```
Recent earthquakes — one in San Francisco in 1989 and another that hit Los Angeles in 1994 — have served as reminders that Californians continue to live in the shadow of The Big One — the major earthquake that experts predict will strike in the next 30 years. It says a lot for the attractions of life in California — and the optimism of those who continue to enjoy it — that despite this dire prediction, millions of people still seek their future in the Golden State’s promised land.
```
**Example 2 Comment:** This option prompts an output to show all lines in the file `California-History.txt` except empty ones. It's useful when we want to skip all empty lines in a file.

---

### For `-r`:

**Example 1 Input:**
```
grep -r "modernity and history found anywhere in the world" written_2/travel_guides/
```
**Example 1 Output:**
```
written_2/travel_guides//berlitz2/Bahamas-WhereToGo.txt:Nassau town has a fine pedigree dating back through colonial times, and the compact town center still has the feel of life under the English. Out in the natural harbor, which offered shelter to many a pirate ship, is a major port that can accommodate 15 large cruise ships at one time. This capacity was created in 1965 when public money was invested to dredge the port, specifically to allow bigger ships to enter. The huge vessels, hundreds of feet high, dwarf the towns buildings, which regulations set at a maximum of three stories, and create one of the most effective juxtapositions of modernity and history found anywhere in the world. The cruise port at Prince George Wharf brings in by far the majority of visitors to the Bahamas.
```
**Example 1 Comment:** This option prompts an output to find all documents in the target directory `travel_guides` and its subdirectories that contain the keyword `"modernity and history found anywhere in the world"`. It's helpful when we wanna find all the files containing a certain keyword in a directory and its subdirectories.

**Example 2 Input:**
```
grep -r "public money was invested to dredge the port" --include="*.txt" written_2/travel_guides/
```
**Example 2 Output:**
```
written_2/travel_guides//berlitz2/Bahamas-WhereToGo.txt:Nassau town has a fine pedigree dating back through colonial times, and the compact town center still has the feel of life under the English. Out in the natural harbor, which offered shelter to many a pirate ship, is a major port that can accommodate 15 large cruise ships at one time. This capacity was created in 1965 when public money was invested to dredge the port, specifically to allow bigger ships to enter. The huge vessels, hundreds of feet high, dwarf the towns buildings, which regulations set at a maximum of three stories, and create one of the most effective juxtapositions of modernity and history found anywhere in the world. The cruise port at Prince George Wharf brings in by far the majority of visitors to the Bahamas.
```
**Example 2 Comment:** This option prompts an output to find all documents which has extension `".txt"` in the target directory `travel_guides` and its subdirectories that contain the keyword `"modernity and history found anywhere in the world"`. It's helpful when we wanna find all the `.txt` files containing a certain keyword in a directory and its subdirectories.

---

### For `-i`:

**Example 1 Input:**
```
grep -i "mONey WAs" written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
```
**Example 1 Output:**
```
Nassau town has a fine pedigree dating back through colonial times, and the compact town center still has the feel of life under the English. Out in the natural harbor, which offered shelter to many a pirate ship, is a major port that can accommodate 15 large cruise ships at one time. This capacity was created in 1965 when public money was invested to dredge the port, specifically to allow bigger ships to enter. The huge vessels, hundreds of feet high, dwarf the towns buildings, which regulations set at a maximum of three stories, and create one of the most effective juxtapositions of modernity and history found anywhere in the world. The cruise port at Prince George Wharf brings in by far the majority of visitors to the Bahamas.
```
**Example 1 Comment:** This option prompts an output to find the line in the target file `Bahamas-WhereToGo.txt` that contains the keyword `"mONey WAs"` regardless of whether it's capitalized. It's useful when we wanna do case-insensitively searching.

**Example 2 Input:**
```
grep -i -w "mONe" written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
```
**Example 2 Output:**
```
// NO OUTPUT
```
**Example 2 Comment:** This option prompts an output to find the line in the target file `Bahamas-WhereToGo.txt` that contains the keyword `"mONe"` as an independent word. In this case, no output is shown because there's no line in the file containing `"mONe"` as an independent word. It's useful when we wanna find lines that contain the keywords that entirely match our input argument.
