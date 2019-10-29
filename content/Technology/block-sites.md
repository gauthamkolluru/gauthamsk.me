---
title: "Automation Series - Article 2: Block Websites"
categories: ["Python", "Automation", "Linux", "Windows"]
date: 2019-10-25T16:00:00+05:30
publishdate: 2019-10-25T20:00:40+05:30
draft: true
---

There are two kinds of procrastinators in humans as categorised by [Tim Urban in one of his Ted Talks](https://youtu.be/arj7oStGLkU) basing on their actions, on the approach of the due date. Type-1, are those who has no reaction even when the due date passes by and the Type-2, are just most of us. We don't react as required when the due date approaches from months remaining to weeks remaining, though we would really want to act on it but as usual we remember some even more important tasks of playing just one last game on our X-Box or watching a last vlog. After about a minute, relatively and at least half a day literally, we realise what had happened. But when the weeks become days and we realise that the tasks definitely needs more time than available, we jump over it and start working on it with no idea of rest of the world, not even day and night. And finally, somehow, we might at least approach it's completion basing on the kind of task and the kind of submission.

Right after the due date, we'd think, "It'd been better if we'd started earlier" and then we might think of being able to block doing the tasks that were taking just a min (relatively) and that's when the idea of being able to block websites incepted. Being passionate about motorcycles and motorcycling myself, I watch a lot motovolgs on [YouTube](www.youtube.com). I can watch them all day for even days together as long as they're showing their ride and their machine. Therefore, I decided, to keep myself away from the vlogs, I have to block those sites for most part of the days and it is then I learnt how to block websites from this article on [GeeksforGeeks](https://www.geeksforgeeks.org/website-blocker-using-python/).

I took the basic idea of what to do from the above mentioned block and customised for my purpose which we shall look into. Again, I'll take a line by line approach.

```python
import time
from datetime import datetime as dt
```

The first part of a python program is just about importing the required packages. Here, I have imported **time**, again for the only reason, to make the program sleep for some time and it's the **datatime** package that the code is essentially dependant on.

Youtube Playlist for [Programming in Python](https://www.youtube.com/channel/UCWeOiQJHuUvcwR8Us5iVnAA?view_as=subscriber)

Github Link to the script: [file-segregator.py](https://github.com/gauthamkolluru/PythonLabs/blob/master/Automation/file-segregator.py)
