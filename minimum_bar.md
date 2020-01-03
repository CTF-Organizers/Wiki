# WORKING DRAFT
## go to #minimum-bar for discussion and feedback

In this page you can find a list of minimum requirements that every CTF competition should have. The target audience for this document is CTF organizers that wish to organize a CTF competition that follows the expectations of players in the community. If a requirement can't be met for some reason, players should know.

# Format and Mechanics
CTF competitions follow well understood mechanics, as such, it is important that when someone announces a CTF competition open to the public it satisfies players expectations. In specific, when someone uses the terms **Jeopardy-style CTF** or **Attack-Defense CTF**, they should follow the mechanics expected in such competitions. Deviations from these mechanics should be explicitly declared up-front, so players are not surprised when they start playing.

The minimum bar **requirements** for **all CTF competitions** are: The competition should be announced to players early on (at least 2 weeks ahead of time), and it should include the categories of the competition, an approximate number of challenges, and a definite starting time and duration. Organizers should provide a channel in which players are able to quickly reach out to and communicate problems (with tasks or infrastructure), and organizers should be responsive during the competition.

The mechanics **requirements** of a **Jeopardy-style CTF** are as follows: The competition presents players a list of challenges. The challenges should at least be labelled by category. Solving the challenge should reveal the player a flag, which follows a predictable format (defined for the competition as a whole, or per-task), and which players can submit to the organizers for points, the form in which points is calculated should be simple. Challenges should either all be released either all at once, or gradually. If released gradually, players should be able to know if all challenges have been released or more will be released in the future.

The mechanics **requirements** of an **Attack-Defense CTF** are as follows: The competition presents players with a list of vulnerable applications. Every team has the same applications, and exploiting the vulnerability in another team's instance gives out a flag. Points are awarded for stealing a flag, and/or reduced for getting a flag stolen from your own instance. Keeping the instances running and accessible to other players is also considered in the score.

## Recommendations
* [CTFtime](https://ctftime.org) is the de-facto authoritative list of CTF competitions. Most players expect public CTFs to be announced there with 3 weeks or more ahead of time. Exceptions might include non-competitive, advertising, or training competitions.
* The usual flag format for a CTF consists of a short prefix followed by a secret string. The secret itself usually has a predefined maximum length (eg, 1,000 bytes), and a predefined alphabet (eg, `[a-zA-Z0-9!$%^&*()=+@~#'/?><.,|_-]`) for example`CTF{This_Is_A-top-Secret!_;)}`. It's preferable, but not always the case, if scoreboards trims white-space and accepts flags being case insensitive, and avoids letters that can cause confusion, unless part of the challenge (eg, l vs. I). See more advice on flag format [here](https://github.com/pwning/docs/blob/master/suggestions-for-running-a-ctf.markdown#flag-format).
* Usually the list of teams that solved each task is public. In those cases, players usually expect to be able to know how many teams are actively participating. As such, having a task that players just have to copy-paste to mark they are active is helpful.
* The duration of CTF competitions usually is 48 hours during a weekend. There are exceptions to this rule, but that will change the expectations of the teams playing.
* Most CTFs have challenges in categories pwn, web, crypto, and reversing. It is possible for a task to be in more than one category.
  * Pwn usually has something to do with binary exploitation (memory corruption).
  * Web usually has something to do with HTTP services (XSS, SQL injection, etc).
  * Crypto usually has something to do with crypto implementation or design flaws.
* Tasks should be scored using static scoring (organizers define number of points ahead of time), or a known and tested dynamic scoring formula (points changes based on number of solves).

# Task Quality
There will be a significant amount of human-hours spent in the competition, as such, it is a strict requirement that the tasks satisfy some basic quality requirements. While the design of a good CTF task is not trivial to codify in a list of requirements, there are some obvious steps organizers should take to attempt to keep a minimum quality bar.

The minimum **requirements** for **designing a task** are: The task should be designed with an intended known solution in mind. The task should be original, and not reuse an existing problem presented elsewhere that some players might have already solved beforehand. The author should have a well thought-out argument on how players are expected to discover all required aspects of the task, even if unfamiliar with the technology. If a task has too many possible ways to approach it and no logical mechanism to discover the right solution, the task description should point players to the right path, as to avoid luck being the defining factor on who solves the task.

The minimum **requirements** for **implementing a task** are: The task should have a way to test it is solvable (an existing exploit). The task should be tested in the exact same environment players will be solving it. The task implementation should be at least reviewed by another person (different than the author), that can follow the logical sequence of events that leads to the solution, looking for any leaps in logic or guessing. The task implementation should be tested to work and be solvable with at least the expected number of players.

## Recommendations
* [The Many Maxims of Maximally Effective CTFs](http://captf.com/maxims.html) contains general design advice on how to select and design problems for CTF tasks.
* [CTF Design Guidelines](https://ctf.guide) includes in-depth task design guidelines and a description the qualities of good CTF tasks.
* [PPP suggestions for running a CTF](https://github.com/pwning/docs/blob/master/suggestions-for-running-a-ctf.markdown#problems) contains more practical advice on the design and implementation of tasks for different categories.

# Fairness
In a competitive environment, CTF players expect to all have the same starting foot, where only previous knowledge, experience, and effort are used as a differentiating factor. As such, there are some basic requirements that ensure that a competition is fair to all contestants.

The minimum **requirements** for **fairness** are: All information should be public to all players at the same time. Any communication from organizer to player that can hint to any new information should, without exception, also be known to all players. If the competition is online and global, organizers should make sure that regardless of the timezone a player uses, they should have the same ability to earn points (in the case first-blood bonus points or speed-runs are used).

# Stability
Given the time-limited aspect of CTF competitions, a slight disruption on the availability of a task can affect the fairness and experience of the competition. Either malicious (DoS) or accidental downtime should be planned for ahead of time by the organizers, and some minimum requirements regarding the stability of the infrastructure, including both the scoreboard and the tasks.

The minimum **requirements** for **stability** are: Organizers should have an independent communication channel to players (IRC, or similar) independent of their own infrastructure. Links to the tasks that don't require online services for working on (eg, reversing, pwnable) should be published in case of long-term downtime. Organizers should do some amount of load-testing of the challenges, with the expected number of players.
