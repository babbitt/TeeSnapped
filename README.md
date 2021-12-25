# TeeSnapper
### :exclamation: Do you work at TeeSnap? Let's talk, see below
## How it works
1. Enter in your information
    * Subdomain (the part of the url before `.teesnap.net` (eg. `test.teesnap.net`'s subdomain would be `test`))
    * Course ID (this is harder to find, it's in the URL when you go to book)
    * Number of holes
    * Number of players
2. Click `Generate Link`
3. Drag the link labelled `Reservation Tool [DATE]` to your bookmarks bar
4. To to the teesnap booking link
5. Click on the newly created bookmark

## Why it works
TeeSnap has a vulnerability in their software that allows you to book up to x+1 days in advance instead of x (whatever is allowed at the club [usually 7]). This utilizes their publicly accessible `customer-api` (`teetimes-day` api endpoint) to get a schedule of the days tee times and then formats a checkout URL with the first available tee time that isn't booked or held.

## Should I worry about using TeeSnapper?
**_Like, Maybe?_** The reality is that this is a publicly accessible api and anybody with the knowhow could execute this. I'm just making it much more accessible. That being said it's probably not something they're thrilled about. If they wanted to let you book another day in advance, they would probably just let you.

## What about Mobile / The bookmark tool isn't working for me
If you find that TeeSnapper isn't working for you, it may be worth trying the manual version of the application. To do so, type `?manual=true` at the end of the URL. Eg `https://joebabbitt.com/TeeSnapped/?manual=true`. You'll have to disregard the instructions listed as they're different, you'll figure it out.

## I work at TeeSnap
Hi. Hopefully this little tool is cool w y'all. I wrote it for educational purposes as a real world example of basic API manipulation. If it's not contact me @[Joebabbitt.com](https://joebabbitt.com) and we can square something away. I'd happily accept a bug bounty if you're feeling generous or even consult on how to fix this issue. There were some other vulnerabilities I noticed with this endpoint but I didn't poke any further so I'd also be happy to take a look for you.