# Using the hotelling line in a closest-guess wins game

### 1. Intro

Imagine you are with you friends at a formal event, say a wedding, graduation or a prize giving ceremony. There will inevitably be many (potentially long and potentially boring) speeches. What better way to liven up the situation by guessing how long the speech will last. Lose, and you've sat through a long and boring speech thinking about other things just to listen to your friend crow about having the closest guess, but win and you've got bragging rights for the rest of the day. Economics may get a bad rep about being too theoretical and failing to be useful in real situations, but here an economic theory from the 1920s could actually help you out. First published in 1929, The hotelling model aims to explain why it is rational for companies to make very similar products despite the possibility of lots of variation[$^1$](https://en.wikipedia.org/wiki/Hotelling%27s_law). However, here we can use very similar logic to boost your chances of winning the closest guess game, and salvaging some enjoyment from the sitting through the speeches without any risk of being caught checking sports scores. 

The aim of the game is simple - closest guess to the correct duration of the speech in question wins. To start off with most people can get some sense of what the minimum and maximum duration of the speech is likely to be, with their next step being to randomly guess somewhere between these two numbers with some adjustment made for how rambling the speaker in question is. But can we do better using economics to maximise your chances of winning?

### 2. A sequential game

To start off with have a very simple game. It's just you and the person next to you. One of you makes your guess, and the other one will guess in response. In economics we can refer to this as a 2-player sequential action game. We'll also make the simple assumption that you don't know the speaker, so each value between the minimum and maximum duration are equally likely (i.e. the distribution of speech distribution is uniform).

Your friend guesses first, guessing $x_1$ which is pretty close  to the upper end of the possible range of values.

*TODO Uniform distrubtion image with guess 1*

You think this guess is way too high, so you're tempted to make a guess towards the other end of the scale, say $x_{\text{low}}$. $x_{\text{mid}}$ is then the value halfway between you and your friend's guesses (i.e. the duration at which the outcome would be a draw). 

*TODO Uniform distribution image with guess 1 and guess low*

In this case we can see that any durations to the right of $x_{\text{mid}}$ result in your friend winning, and any guesses less that $x_{\text{low}}$ lead to you winning. We can also see that by slightly increasing your guess, you can increase the range of values for which you win. All values less than your guess you win, and you win half of the guesses between your guess and your friend's. Applying this logic further, you can maximise your chances by making this area that is split as small as possible. You therefore do best by guessing the value right next to your friend's guess i.e $x_1 - \epsilon$ where $\epsilon$ is an arbitrarily small number. 

*TODO Winning guess diagram*

So if your friend guesses 12 minutes and 17 seconds, you guess 12 minutes and 16 seconds. It is now more than likely that you will win, and any accusations of *"being boring"* can be used as clear signs your friend is a sore loser for the rest of the evening. 

Now in this setup there are clear advantages to guessing second (what economists call a first mover disadvantage). This is because the first player is having to choose a value they think is most likely from a large range of values. The second player simply has to decide whether they think the actual value is bigger or smaller than this first guess - a far easier task! So what should you do in the unfortunate case of having to guess first?

Well knowing that your friend, if they have any sense, will pick a value right next to your guess, you want to minimise their chance of winning. Or in other words, minimise the range of values for which their guess is closest. You can achieve this by picking the average value, and going bang in the middle of the minimum and maximum value. As a result you both have 50% chance of winning, and you have turned your first mover disadvantage into a evens chance of winning - not at all a bad outcome! This result can be proven as follows.

*TODO backward induction to 50/50 diagram*

If you were to choose a value that wasn't in the middle, say $x_a$, then your friend would choose $x_b$ and be in a much better chance of winning. But you would then be better off choosing $x_c$, and in return your friend would choose $x_d$. Continuing this hypothetical chain, you can see that the only value for which you are no better off by changing your guess in response to your friends guess is when you choose $x^*$ at halfway. Here, no player can be any better off by changing their guess given what the other player has guessed, and thus this is a stable outcome (or as economists say, a *nash equilibrium*[$^2$](https://en.wikipedia.org/wiki/Nash_equilibrium)). This approach of thinking through hypothetical repeated steps until you get to a stable outcome is going to be useful for solving more complex versions of this game.

### 3. Multiplayer game

For instance now let's assume that another of your friends wants to get in on the fun. 






### Sources

1. https://en.wikipedia.org/wiki/Hotelling%27s_law (Visited 16/05/24)
2. https://en.wikipedia.org/wiki/Nash_equilibrium (Visited 16/05/2024)