# Lab Report 3: Researching Commands
## Choose of Commands: `prep`
1. `-v` : This option stands for "invert match," and it tells `grep` to only display lines that do not match the specified pattern.
2. `-r` : This option stands for "recursive," and it tells `grep` to search through all files and directories in the specified directory (or directories).
3. `-i` : This option stands for "ignore case," and it tells `grep` to perform a case-insensitive search.
4. `-c` : This option stands for "count," and it tells `grep` to display only the number of lines that match the specified pattern.
## Examples and Breakdowns
### For `-v`:

**Example 1A Input:**
```
grep -v "the" written_2/travel_guides/berlitz2/California-History.txt
```
**Example 1A Output:**
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
**Example 1A Comment:** This option prompts an output to show all lines in the file `California-History.txt` that doesn't contain the keyword `"the"`. It's useful when we wanna find lines that don't contain a certain keyword.

**Example 1B Input:**
```
grep -v "^[[:space:]]*$" written_2/travel_guides/berlitz2/California-History.txt
```
**Example 1B Output:**
```
A Brief History
The first wave of California immigrants arrived somewhere between 20,000 and 35,000 years ago — wandering Asiatic tribes who entered the American continent via the Bering Strait, which at that time was dry land, or perhaps covered in ice. In the succeeding centuries, their descendants continued to push south and east, and eventually spread out to people the whole of the continent from Alaska to Patagonia. The tribes who decided to settle in what is now California were fortunate in their choice of homeland. The climate was very pleasant, and food was sufficiently plentiful for them to avoid the constant warfare that plagued many tribes elsewhere in the Americas.
```
...
```
Recent earthquakes — one in San Francisco in 1989 and another that hit Los Angeles in 1994 — have served as reminders that Californians continue to live in the shadow of The Big One — the major earthquake that experts predict will strike in the next 30 years. It says a lot for the attractions of life in California — and the optimism of those who continue to enjoy it — that despite this dire prediction, millions of people still seek their future in the Golden State’s promised land.
```
**Example 1B Comment:** This option prompts an output to show all lines in the file `California-History.txt` except empty ones. It's useful when we want to skip all empty lines in a file.

---

### For `-r`:

**Example 2A Input:**
```
grep -v "the" written_2/travel_guides/berlitz2/California-History.txt
```
**Example 2A Output:**
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
**Example 2A Comment:** This option prompts an output to show all lines in the file `California-History.txt` that doesn't contain the keyword `"the"`. It's useful when we wanna find lines that don't contain a certain keyword.

**Example 2B Input:**
```
grep -v "^[[:space:]]*$" written_2/travel_guides/berlitz2/California-History.txt
```
**Example 2B Output:**
```
A Brief History
The first wave of California immigrants arrived somewhere between 20,000 and 35,000 years ago — wandering Asiatic tribes who entered the American continent via the Bering Strait, which at that time was dry land, or perhaps covered in ice. In the succeeding centuries, their descendants continued to push south and east, and eventually spread out to people the whole of the continent from Alaska to Patagonia. The tribes who decided to settle in what is now California were fortunate in their choice of homeland. The climate was very pleasant, and food was sufficiently plentiful for them to avoid the constant warfare that plagued many tribes elsewhere in the Americas.
```
...
```
Recent earthquakes — one in San Francisco in 1989 and another that hit Los Angeles in 1994 — have served as reminders that Californians continue to live in the shadow of The Big One — the major earthquake that experts predict will strike in the next 30 years. It says a lot for the attractions of life in California — and the optimism of those who continue to enjoy it — that despite this dire prediction, millions of people still seek their future in the Golden State’s promised land.
```
**Example 2B Comment:** This option prompts an output to show all lines in the file `California-History.txt` except empty ones. It's useful when we want to skip all empty lines in a file.

---
