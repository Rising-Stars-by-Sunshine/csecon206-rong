# # Title Trust Game Dessigned by Rong (https://www.nature.com/articles/s41562-021-01152-2)
## Project information
- **Author**: Rong Cong,Political Economy, 2024, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Problem Set No. or Final Project for [COMPSCI/ECON 206 Computational Microeconomics, 2023 Spring (Seven Week - Second)](https://ce.pubpub.org/) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: I would like to thank Prof. Luyao Zhang for her wonderful curriculum setting and instructions on CSEcon 206.Thank Yiyuan very much for helping me deep understand Otree.


## Table of Contents

- model
- code
- spotlight
- more about the author
- references

### Model
- Game Environment:

This trust game is a model of the game used to study trust, reciprocal preference, altruistic preference and egoistic preference.
In the version of the game I designed, there were two anonymously matched players, named A and B, playing the role of real life principal and agent. There are two rounds of the game with similar rules. After the first round, players are allowed to know the outcome of the first round and the strategy chosen by their opponents in the first round. Therefore, they can adjust their strategy in the second round. That is, in my current hypothesis, the strategies chosen by both players in the first round will directly affect the strategies chosen by both players in the second round and the level of trust between players.
At the beginning of the game, A has $1,000 and B has $0. A has to choose whether or not to give B some of his money, which I'll call X. B, knowing A's choice, can choose whether to get double or triple X, which is 2X or 3X. If A chooses to receive 2X, he has no mandatory requirement to return A certain amount but is free to choose whether or not to return A portion of his money, which I'll call Y. If A chooses to get 3X, then he is forced to give back at least 1.5X. That is, if A chooses to get 3X, then he is forced to return to A at least 1.5X+Y. The value of Y can be determined by B himself (it must be greater than or equal to 0). At the end of the first round, both players immediately know the other's choice and their existing balance, and then play a second round with exactly the same rules.

Possible strategies for Player A：

1. win-win situation: In both rounds, A trusts B to give back half of the profits, so A gives all the money to B.

2. risk minimization: Don't trust B in both rounds and don't pay B any money at all. The end of the game guarantees A $1,000.

3. Compromise:

   1) High risk. Trust B and give B some money in the first round, and if B chooses to give back A portion of the proceeds (greater than what A gives to B), continue to trust B in the second round. If B fails to keep his promise in the first round, no money is given to B in the second round. 

   2) Less risk. Trust B and give B some money in the first round, and if B chooses to return A portion of the proceeds (greater than what A gives B), betray B in the second round and give B no money at all. If B fails to keep his promise in the first round, he gets nothing in the second round.
   
Possible strategies for Player B:

1. win-win situation: In both rounds, B chooses to multiply the amount of money given to him by A by three times and return it to A by half. If this can be done in each round, the sum of the benefits will be maximised. Eventually, the two sides will be able to split the proceeds.

2. Profit maximization: Convince A to cooperate in the first round and give all of his money to B, who keeps his word and chooses to triple the money A gives him and return half of it to A. In the second round, A is still persuaded to give all the money to B, but B betrays A. B chooses to double the money A gave him and does not give any money back to A.

3. Compromise: Once A chooses to give B A certain amount of money (which B needs to convince A to do), whatever choice is made returns A certain amount of money so that A's total amount of money at the end of the round is greater or equal to that at the beginning of the round.


Payoffs：

1. Win-win situation: All players choose to trust each other, player A chooses to give all of his money to Player B, and Player B chooses to triple the money given by Player A and return half of it to Player A. If this can be done in each round, the sum of the benefits will be maximised. Eventually, the two sides will be able to split the proceeds.
2. The choice B made in order to gain A's trust in the second round. AB trusts each other in the first round, Player A chooses to give all of his money to Player B, and Player B chooses to triple the money A gives him and return half of it to Player A. But in the second round, B betrays A and chooses to double the amount of money A gives him, so that he doesn't have to give A any money and maximizes his own profit.
3. Compromise: A trusts the other person and gives B a certain amount of X1 in the first round. B chooses to double the amount of money A gives him and give A a certain amount of Y1 (Y1 is greater than X1). A chooses to continue trusting the other party and gives B a certain amount X2 in the second round. B chooses to multiply the amount of money that A gives him by 2 and give A a certain amount of Y2.

4. A completely distrusts B and sees B as a purely rational person. In this case, A won't give B any money, so A can make sure he still has $1,000 at the end. But at this point, the sum of the benefits is the least.

5. A trusts the other person and gives B a certain amount of X1 in the first round. B betrays A and chooses to double the amount of money A gives him. In the second round, A still chooses to trust B and still gives B A certain amount X2. B still betrays A and chooses to multiply the money A gives him by two times. In this case, B is going to get a bigger payoff.

6. A trusts the other person and gives B a certain amount of X1 in the first round. B betrays A and chooses to double the amount of money A gives him. In the second round, A chose not to trust B and pay B any money, so that in fact nothing changed in the second round, the outcome of the game was decided at the end of the first round.
- Solution Concept

Based on an analysis of payoffs, it's easy to see that A and B can only maximize their overall benefits when they both trust each other completely through two rounds of the game. It's worth noting that I don't think either A or B, as rational thinking individuals, would choose to betray each other right away in the first round. Because they betray each other in the first round, they will not be able to trust each other in the second round and will use extreme measures to maximize their personal interests in the second round. Interestingly, because there is no third round, the sense of trust has lost its meaning in this round of cooperation. Under these circumstances, would A and B really choose to trust each other in the second round? That's probably what I'm trying to study in this experiment based on how people actually react.

- Evaluations: e.g. efficiency and fairness

In this experiment, A and B are relatively unfair, because if A chooses to minimize the risk, he will not give any money to B, thus ensuring that he has at least $1000. However, for B this would mean that his payoff would be 0. So B needs to make A believe in herself in some way, such as giving back more money after A gives A certain amount of money in the first round, or negotiating with A and keeping his promise before the game starts. In my opinion, B is in a relatively passive position in the game, and B needs to persuade A not to pursue the most conservative option with more money. A, on the other hand, needs to accurately judge and distinguish B's real intention if he wants to make more money.

### Code

The customized game changed three things from the original game. First, the endowment went from 100 to 10,000. Second, the multiplier went from 3 to 10,000. Third, custom games collect the gender and age of the player and the socio-cultural environment of the simple player before the game starts.I will introduce the reasons for my modification in detail below.

Explanation

Traditional research suggests that in general, the more initial endowment, the more likely Player A is to choose to share, while Player B is more likely to share some or all of their endowment with Player A (Charness et al. 2005). This is because the amount of initial endowment affects Player A's expected earnings and risk perception. If the endowment is high, Player A will be more likely to bear the risk of sharing and will have more confidence in obtaining higher returns. For Player B, the amount of endowment also affects their expected earnings and risk perception. If the endowment is high, they will be more likely to share because they believe in Player A's sharing behavior and higher returns (McCabe et al. 2003). In the customized game, the initial endowment is set at $10,000, a relatively considerable amount. In estimating and assuming the game results, Player A is expected to share at least some of their endowment with Player B. This makes any choice not to share the initial endowment very interesting and worth studying.

Berg, Dickhaut, and McCabe's classic study found that the higher the multiplier, the higher the sharing rate of players in the trust game (Berg et al. 1995). At the same time, Bohnet and Zeckhauser's research also found that a high multiplier can increase trust and returns, thereby reducing untrustworthy behavior (Bohnet et al. 2004). Based on these studies, the multiplier in the new trust game will reach 10,000. This means that the potential benefits of choosing to trust the other player will become incredibly huge, and any small changes in the sharing of funds will bring about huge changes in the results. The customized game hopes to see how much risk people are willing to take under infinite temptation.

Gender is expected to affect the level of trust between players in the trust game. First, there are some differences between men and women in terms of socialization, which may affect their behavior in the trust game. For example, some studies have shown that women's brains are more adaptable to social and emotional stimuli, while men's brains are more adaptable to spatial and motion stimuli (Baron-Cohen et al. 2005). Women pay more attention to the intimacy of interpersonal relationships, so they attach more importance to the trust and care of the other party, while men tend to seek greater returns through adventure (Baron-Cohen et al. 2005). Secondly, societal expectations of men and women may also affect their behavior in the trust game. For example, some studies have shown that society tends to view men as more confident and adventurous, so men may be more inclined to take risks in the trust game (Bosson et al. 2000). However, other studies have pointed out that there are differences in the behavior of men and women from different cultural backgrounds in the trust game, but gender itself does not have a significant impact on trust behavior (Croson et al. 1999). Therefore, whether gender affects players' choices is one of the factors that the game hopes to analyze through sufficient data collection.

Age is expected to influence the level of trust between players in the trust game. Participants who are older tend to exhibit higher levels of trust in the trust game, which may be related to a more stable and conservative mindset that develops with age (Cappelletti et al. 2011). However, some experiments have shown that age does not significantly affect behavior in the receiving phase, possibly because participants are more focused on their own interests during that phase (Cappelletti et al. 2011). Through sufficient data collection, customized games will link age with social and cultural environments as well as gender, attempting to further analyze the influence of gender on the level of trust.

The impact of social and cultural environments on trust between players in the trust game has been almost fully established. For example, Gelfand et al.'s research explored cultural differences in 62 societies and linked these differences to individuals' trust behavior in the trust game. The study found that cultural differences in individualism and collectivism significantly influence the level of trust between players in the trust game (Gelfand et al. 2004). In an individualistic cultural environment, people tend to exhibit more adventurous behavior, focusing more on individual interests and self-expression, which may result in more adventurous behavior. In a collectivist cultural environment, people place more emphasis on long-term interests and stable relationships, which may result in more conservative behavior (Gelfand et al. 2004). Therefore, before the game starts, customized games will ask players to briefly describe their own social and cultural environments as a reference for analyzing their behavior. Since social and cultural environments are a large category that cannot be comprehensively collected in a short period of time, this information is important but only serves as a reference.
- oTree Experimental Code 


### Spotlight
- Behavioral experimental paper：Fowler, James H., and Nicholas A. Christakis. "Cooperative behavior cascades in human social networks." Proceedings of the National Academy of Sciences 107, no. 12 (2010): 5334-5338.

What research question does the behavioral experimental research intended to address?

The behavioral experiment was designed to explore non-economic considerations of trust behavior, such as emotional and social factors, and how these affect how people behave in trust games. Specifically, the authors focus on three research questions: 
i. Do people take into account each other's emotional states during trust games? 
ii.  Are people affected by social factors in the trust game? 
iii.  What are the effects of these non-economic factors on people's trust behavior?

### More about the Author

   
 ![image](WechatIMG46.png)
 
 As a junior majoring in political economy, Rong Cong is very interested in economics, anthropology and psychology. She hopes to do enough cross-disciplinary research and study in the future. At the same time, Rong Cong is also a music lover. This is a cover of her song 👉🏻https://y.music.163.com/m/artist?app_version=8.9.61&id=46956986&userid=1572161264&dlt=0846.
   
### References

- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.

```
@article{levin2022bridging,
  title={Bridging level-k to nash equilibrium},
  author={Levin, Dan and Zhang, Luyao},
  journal={Review of Economics and Statistics},
  volume={104},
  number={6},
  pages={1329--1340},
  year={2022},
  publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…}
}
```

