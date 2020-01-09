# WORKING DRAFT

# Basic CTF Requirements and Recommendations #

**Use #minimum-bar on Slack for discussion.**


## Requirements ##

The following are requirements that every CTF event needs to follow:

1. Event shall be announced at least 2 weeks prior to start
2. Event announcement shall publish all rules, including start/end times, scoring system(s), flag format(s), flag submission guidelines/procedures, and how new challenges/tasks will be released
3. Event organizers shall actively monitor a designated, public channel over which players may communicate problems with tasks/infrastructure over the duration of the event
4. All challenge/task information should be made public to all players at the same time throughout the event. Any new information provided as a response to a question/comment from a team must be provided to all players as soon as possible.


## Recommendations ##

The following are recommendations that every CTF should consider:

1. Event should be announced and listed on [CTFtime](https://ctftime.org), the de-facto authoritative list of CTF competitions. Exceptions might include non-competitive, advertising, or training competitions.
2. The usual flag format for a CTF consists of a short prefix followed by a secret string. The secret itself usually has a predefined maximum length (eg, 1,000 bytes), and a predefined alphabet (eg, `[a-zA-Z0-9!$%^&*()=+@~#'/?><.,|_-]`) for example`CTF{This_Is_A-top-Secret!_;)}`. It's preferable for scoreboards to trim white-space, accept flags case-insensitively, and avoid symbols that can cause confusion (eg, l vs. I vs. 1). See more advice on flag format [here](https://github.com/pwning/docs/blob/master/suggestions-for-running-a-ctf.markdown#flag-format).
3. The list of teams that have solved each challenge/task should be public.
4. Challenges/tasks should be scored using static scoring (organizers define number of points ahead of time), or a known and tested dynamic scoring formula (points changes based on number of solves).
5. Challenges/tasks should be designed with an intended solution in mind. This intended solution should be tested prior to the event, ideally as a script that can also be re-run to confirm the solution works during the event at any time.


## Resources ##

The following are useful, additional resources that we believe are generally
beneficial for CTF organizers to review:

* [The Many Maxims of Maximally Effective CTFs](http://captf.com/maxims.html) contains general design advice on how to select and design problems for CTF tasks.
* [CTF Design Guidelines](https://ctf.guide) includes in-depth task design guidelines and a description the qualities of good CTF tasks.
* [PPP suggestions for running a CTF](https://github.com/pwning/docs/blob/master/suggestions-for-running-a-ctf.markdown#problems) contains more practical advice on the design and implementation of tasks for different categories.
