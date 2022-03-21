# Prep: Readings ... Get Ready for 401

Read the articles and watch the videos referenced in the Reading and Reference Materials section of the prework guide below.

## Assignment Instructions

Go through the reading material for this class and watch/bookmark the additional resources provided. Prepare an entry for your Readings Notes Repository that summarizes the principal reading topic as though you were presenting the material to someone new to the industry.

### Article/Entry Ideas

- Blog Article (2-3 paragraphs with code sample)
- Dictionary / Flash Cards
- Notes in outline form
- Use an analogy
- Explain a detail in depth
- Use WHY, WHAT, HOW structure
- Tutorial / walk through an example as though you were teaching a 102 student
- Write a quiz
- Create a vocabulary/definition list
- Write a cheat sheet
- Create a diagram / visualization / cartoon of a topic
- Anthropomorphize the concepts, and write a conversation between them
- Build a map of the information
- Construct a fill-in-the-blank worksheet for the topic

### To submit this assignment

- Create a new markdown file in your reading notes repository, and add your notes
- If you utilize any content directly from the reading sources, be sure to identify what you are quoting, and cite the source
- Add a link to this new file under the table of contents for this course
- Then ACP your main branch to create a rendered web page on GitHub pages
- Copy the rendered content and paste it into the discussion
----
- [x] [Solving Problems](https://simpleprogrammer.com/solving-problems-breaking-it-down/)

The author John Sonmez recommends to the reader a six-step process that can be used for any algorithm type programming solution, with the added caveat that one should spend 70% of one's time in the first 3 steps.  The steps are listed as follows:

1. Read the problem completely twice.
2. Solve the problem manually with 3 sets of sample data.
3. Optimize the manual steps.
4. Write the manual steps as comments or pseudo-code.
5. Replace the comments or pseudo-code with real code.
6. Optimize the real code.

The fact that Code Fellows requires all 401 students to read this article written in 2011 demonstrates how valuable this particular strategy still is today in the job of coding or in whiteboard interviews.

- [x] [Act like you make $1000/hr](https://web.archive.org/web/20201018073012/https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d)

First of all, I found the link listed in the assignment to be dead.  medium.com says the author deleted the article.  However, with a little googling, I was able to find the article archived before it was deleted on archive.org. The active link is https://web.archive.org/web/20201018073012/https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d.

The article points out to the reader that being productive is not as a result of just being busy but being focused.  One should not be busy or stressed, but focused, in order to be successful. 

Also, it is important one educates others that your time is expensive, important, and valuable, in order to change their behavior on how they should value the time spent with you. In other words, treat your time as a valuable commodity, so that others will also treat your time in the same manner.

The article also states that "really successful people say no to most things, because most things won't get them to where they truly want to be."

The article concludes by saying that if you value your time at what it deserves to be, you'll complete more important and productive work (and do less trivial and mindless tasks).

- [x] [How to think like a programmer](https://medium.freecodecamp.org/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2)

The article highlights four steps when encountering a new problem:
1. Understand. Make sure you know what is being asked (translate into simpler language if original language unclear) (create visual aids if needed to gain an understanding of the problem)
2. Plan. (to make a good plan, answer the question, 'given input x, what are the steps necessary to return output y?')
3. Divide. Identify the smaller problems contained in the big problem until size of each problem is manageable enough to solve, solve each and every smaller problem, and then join all solutions back together.
4. Stuck? Try three things:
    1. Debug (retrace steps and find where solution went wrong)
    2. Reassess (change perspective by taking a step back or something else)
    3. Research (google)

Lastly, practice this process repetitively in order to improve. Encounter many problems to get better.

- [ ] [The 5 Whys](https://www.mindtools.com/pages/article/newTMC_5W.htm)

The article introduces a type of analysis called 5 whys analysis.  This type of analysis is good for troubleshooting, quality improvement, and problem solving.  The 5 Whys analysis is most effective when resolving simple or moderately difficult problems. The 5 Whys analysis is not the most effective approach though for complex or critical problems, when there could be multiple causes for complex problems and the 5 Whys may falsely  lead you to pursue a single or limited number of tracks of inquiry, when many more tracks of inquiry would be required for a complex or critical problem.

The article then shows how to use the 5 Whys analysis:
1. assemble a team
2. define the problem
3. ask the first "why?"
4. ask "why" four more times (very quickly, to avoid jumping any conclusions prematurely)
5. know when to stop (when asking why produces no more useful responses - usually indicates you have discovered the roote cause of the problem)
6. Address the Root Cause(s) - by agreeing on the countermeasures
7. Monitor your measures

Frankly this process looks stikingly similar to practices I learned in the US Army.  The article does say  "this process was originally developed by the military to assist commmanders in gaining a comprehensive understanding of any fact, problem or situation."

- Recognize and define the problem
- Gather information
- Develop possible solutions to the problem
- Analyze possible solutions
- Select the best solution
- Implement the solution and assess results

FM 5-0 The Operations Process (2010) Department of the Army, US

Seems 5 Whys is cited in the US Army Red Team Handbook page 81 https://usacac.army.mil/sites/default/files/documents/ufmcs/The_Red_Team_Handbook.pdf 

The handbook mentions the 5 Whys is often used as part of the Lean Six Sigma process.

#### Watch these videos

- [ ] [what the heck is the event loop anyway](https://www.youtube.com/watch?v=8aGhZQkoFbQ)

A 26 minute 52 second video on youtube presented at jsconf.eu September 13-14, 2014, by Philip Roberts, a non-programmer.

He answers the question of the title of the talk "what is the event loop", 14 minutes into the 26minute presentation.  

He says that the event loop has the job of looking at the stack and looking at the task queue. If the stack is empty, the event loop takes the first thing on the task queue, and pushes it onto the stack, which gets effectively gets run by the stack.

He further mentions later in the presentation that the event loop also has the job of not only looking at the queue, but more specifically what type of queue, as there is a render queue, and there is a callback queue.  A render can have the side effect of getting delayed if there is too much synchronous code being run (for example a while loop for half a second).  A render queue does however not have the problem of delay when callbacks get added onto the callback queue, because the event loop gives the render queue higher priority over the callback queue when the event loop sees the stack is empty.


- [ ] [The Super Mario Effect](https://www.youtube.com/watch?v=9vJRopau0g0)

This video is a ted talk 15 minutes long. 

Mark Rober the presenter makes one point:

The trick of learning more and having more success is finding the right way to frame the learning process(reference bookmark 2:30 of 15:08 video). Don't get discouraged at smaller failures towards the longer goal. Just continue to work rapidly until you see failures turn into successes incrementally to eventually reach the desired long goal.

When referring to Super Mario Bros the video game, the same point applies: in order to win the game, is not focus so much on how you got there or how many lives you lost or how many points you gained, but to focus on rescuing the princess.  That is what the presenter and his friends adapted to doing in order to learn more and have more success.

He used examples from his life by building painstakingly variations on popular toys and games that allowed the user to win more and have more fun, that won him fame including a demonstration on Jimmy Kimmel's late night talk show with his dartboard that always finds the bullseye for a user that throws errantly at the board.

His main point was defining what he called "The Super Mario Effect", as reiterated 14:33 minutes into the video:

The Super Mario Effect = Shifting the focus from falling into pits to saving the princess, to stick with a task and learn more.

"By shifting your focus to the princess, and treating your life's challenges like video games, you can trick your brain and and actually learn more and see more success" 
  - Mark Rober, former NASA engineer

  14:55 into the 15:08 youtube video

