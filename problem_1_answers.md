For contributors visualization

The audience is project managers and the public who want to see who is committed to the project as well as when these commits are being done. For example looking at the example provided one could quickly tell mbostock performs most of the commits and have done so for the past three years.

To grab the information from the GitHub API the call would be https://api.github.com/repos/{ownerofrepo} /{repo} /contributors 
This call would give you the contributors to that certain repo and how many contributions one has made then you can call commits by contributor with the code 
GET /repos/:owner/:repo/stats/contributors

Also one could use
GET /repos/:owner/:repo/stats/participation 


To get the weekly commit count for the repository owner and everyone else.


If a contributor pushes many commits at the same time there would be a spike during that day for commits for that user. One can address this use by simply scaling the spike to a certain amount or making the spike darker.




For commits visualization

The audience is project managers and project users or visitors who want to see who is how many commits were submitted during the last week as well as year or so.  For example looking at the example provided one could tell that there were a lot of commits during March of 2013.

To grab the information from the GitHub API the call would call

GET /repos/:owner/:repo/commits

Then use the parameter “since” to specify a date range

If a contributor pushes many commits at the same time there would be a spike as well during that day or time period for commits. One can address this use making those commits seems like they belong to a month for example or simply scaling it doing sort of like by doing a logarithmic range.



For code frequency visualization

The audience is project managers as well as project users who want to see who is how stable the code and how active it is as well.  The visualization lets you see the frequency of additions to the code as well as deletions. For example looking at the example provided one could tell that there were many deletions during September of 2011 but many additions during March of that same year.

To grab the information from the GitHub API the call would call

GET /repos/:owner/:repo/stats/code_frequency

Then use the parameter “since” to specify a date range

If a contributor pushes many commits at the same time there would be a spike as well during that day or time period for commits. These spikes can actually be seen on the example provided. One can address this use making those commits seems like they belong to a month for example or simply scaling ie. Creating a logarithmic range.


For Punchcard visualization

The audience is definitely project managers and maybe a bit project contributors as well.  The visualization lets you sort of the amount of commits done per day as well as per hour. For example looking at the example provided one could tell that the most work (commits) are done at 10am – 5pm over the weekdays.

To grab the information from the GitHub API the call would call

GET /repos/:owner/:repo/stats/punch_card 


If a contributor pushes many commits at the same time there would be a huge ball during that time as well as large activity during that day. One can address this by scaling ie. Creating a logarithmic range.




For Pulse visualization

The is definitely visitors as well as project users.  The visualization lets you see large announcements as well as latest authors, commits and issues with the project. For example looking at the example provided one knows there are 9 active issues.

To grab the information from the GitHub API the call would call

GET /repos/:owner/:repo/releases 


As well as a couple more calls specified above such as commits by contributor and the authors of those. These seems to combine a lot of graphics .

If a contributor pushes many commits at the same time there would be a spike in commits of that day. One can address this by scaling ie. Creating a logarithmic range.
