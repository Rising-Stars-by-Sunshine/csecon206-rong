## Trust Game Dessigned by Rong
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

### Part1:Model

The Trust game is an experiment aimed at studying human trust and cooperative behavior (Sabbagh&Clara 2008). In this game, there are two participants: investor A and receiver B. Investor A has a certain amount of money and can choose to give some of it to receiver B. This money will be doubled, and receiver B can choose to return some of it to investor A or keep all the money. If receiver B chooses to return some of the money to investor A, then both investor A and receiver B will jointly receive more money. However, if receiver B chooses to keep all the money, then investor A will lose their investment. Analyzing the behavior of the investor and receiver can effectively analyze the psychology of human trust and cooperative behavior in real life.

### Game Environment:

- Set of the players:In the Trust game, there are two players: one is called the “investor” and one is called the "receiver”. The investor has a certain amount of money and can choose to give some or all of it to the receiver. The receiver knows the investor's choice and can choose to allocate the money he receives to the receiver or not.

- Strategies:
In the Trust game, investors can adopt two strategies: trust and distrust. If investors choose to trust, they will choose to give a portion or all of the currency to the receiver, hoping that the receiver will return a certain amount of currency to them. This will bring a certain amount of risk to themselves because the receiver may not return a certain amount of money to the investor. If investors choose to distrust, they will choose not to give any currency to the receiver, so the receiver will not have any return.
The immediate factor that affects strategy is actually the level of trust between players. The more the investor trusted the receiver, the more money they chose to give the receiver.

- Payoffs: In the Trust game, players' payoffs are directly determined by their choices. Generally, because the money invested by the investor to the receiver is multiplied by a certain proportion, if the investor chooses to trust and the receiver chooses to reciprocate, both will receive more money. If the investor chooses to trust but the receiver chooses not to reciprocate, the investor will lose all the money, and the receiver will get all the money. If the investor chooses not to trust, neither will receive any payoff.

### Backward induction
The solution based on backward induction in the Trust game is a solution to the trust and cooperation problem between investors and receivers. This solution is based on the idea of backward induction, which guides one's decision-making by considering the other's possible reactions and outcomes, thereby achieving the best outcome of mutual trust and cooperation (Aumann & Robert J, 1995).

In the Trust game, the solution based on backward induction guides the investor's decision-making by considering the receiver's possible reactions and outcomes. Specifically, the investor will recursively consider the receiver's decision tree to infer how the receiver will make choices. If the investor believes that the receiver will return a considerable amount, then they will choose to trust and give more money or even all the money in the first round, thus achieving the best outcome of cooperation for both parties (at this point, the total final payoff for both parties is maximized). If the investor believes that the receiver will return a relatively small amount (but at least return something), then they will choose to trust and give a small amount of money in the first round, achieving relatively good results for both parties. If the investor believes that the receiver will not return anything, then they will choose not to trust and give the receiver no money in the first round, thereby avoiding their own loss.



### Evaluation

In the trust game, the backward induction solution is effective because it allows investors to make decisions based on their expectations of how the receiver will perform. By considering the possible outcomes of their behavior and the receiver's response, investors can choose the optimal strategy to maximize their payoff.Research shows that the backward induction solution can increase trust and cooperation among participants in trust games (Charness et al., 2002). Compared to participants using random strategies, those using the backward induction strategy are more likely to trust their partners and receive higher payoffs (Charness et al., 2002).


### Efficiency

- The solution based on inverse induction in the Trust game can be considered a fair solution, as it provides an opportunity for both investors and receivers to achieve maximum joint benefit. Through the concept of inverse induction, investors can consider the receiver's decision tree and predict how the receiver will make their choice, thereby providing guidance for making the optimal decision for themselves. The solution based on inverse induction can be viewed as a fair solution because it encourages trust and cooperation between participants while considering the payoffs for both parties and avoiding one person gaining too much advantage.

- Firstly, this approach emphasizes the importance of trust and cooperation as it allows participants to consider the payoff of both parties while considering their own payoff. In this situation, investors must consider how much money to give to the receiver so that both parties can achieve maximum benefit in case of receiving a payoff. Similarly, the receiver must consider whether to reciprocate and decide how much money to return to maximize the joint benefit of both parties.

- Secondly, the inverse induction solution can also avoid one person gaining too much advantage in the game. Because investors must consider the receiver's reaction and possible outcomes, they cannot simply choose a strategy that only cares about their own payoff. Instead, they must consider their relationship with the receiver and how their choice may affect the payoff of both parties. This interdependent relationship helps maintain fairness between participants, thereby maximizing the payoff for both parties.



### Part2：Code

[Customized oTree code](https://github.com/Rising-Stars-by-Sunshine/csecon206-rong/blob/main/hxm-new_project.otreezip)

The customized game changed three things from the original game. First, the endowment went from 100 to 10,000. Second, the multiplier went from 3 to 10,000. Third, custom games collect the gender and age of the player and the socio-cultural environment of the simple player before the game starts.I will introduce the reasons for my modification in detail below.

### Explanation

- Traditional research suggests that in general, the more initial endowment, the more likely Player A is to choose to share, while Player B is more likely to share some or all of their endowment with Player A (Charness et al. 2005). This is because the amount of initial endowment affects Player A's expected earnings and risk perception. If the endowment is high, Player A will be more likely to bear the risk of sharing and will have more confidence in obtaining higher returns. For Player B, the amount of endowment also affects their expected earnings and risk perception. If the endowment is high, they will be more likely to share because they believe in Player A's sharing behavior and higher returns (McCabe et al. 2003). In the customized game, the initial endowment is set at $10,000, a relatively considerable amount. In estimating and assuming the game results, Player A is expected to share at least some of their endowment with Player B. This makes any choice not to share the initial endowment very interesting and worth studying.

- Berg, Dickhaut, and McCabe's classic study found that the higher the multiplier, the higher the sharing rate of players in the trust game (Berg et al. 1995). At the same time, Bohnet and Zeckhauser's research also found that a high multiplier can increase trust and returns, thereby reducing untrustworthy behavior (Bohnet et al. 2004). Based on these studies, the multiplier in the new trust game will reach 10,000. This means that the potential benefits of choosing to trust the other player will become incredibly huge, and any small changes in the sharing of funds will bring about huge changes in the results. The customized game hopes to see how much risk people are willing to take under infinite temptation.

- Gender is expected to affect the level of trust between players in the trust game. First, there are some differences between men and women in terms of socialization, which may affect their behavior in the trust game. For example, some studies have shown that women's brains are more adaptable to social and emotional stimuli, while men's brains are more adaptable to spatial and motion stimuli (Baron-Cohen et al. 2005). Women pay more attention to the intimacy of interpersonal relationships, so they attach more importance to the trust and care of the other party, while men tend to seek greater returns through adventure (Baron-Cohen et al. 2005). Secondly, societal expectations of men and women may also affect their behavior in the trust game. For example, some studies have shown that society tends to view men as more confident and adventurous, so men may be more inclined to take risks in the trust game (Bosson et al. 2000). However, other studies have pointed out that there are differences in the behavior of men and women from different cultural backgrounds in the trust game, but gender itself does not have a significant impact on trust behavior (Croson et al. 1999). Therefore, whether gender affects players' choices is one of the factors that the game hopes to analyze through sufficient data collection.

- Age is expected to influence the level of trust between players in the trust game. Participants who are older tend to exhibit higher levels of trust in the trust game, which may be related to a more stable and conservative mindset that develops with age (Cappelletti et al. 2011). However, some experiments have shown that age does not significantly affect behavior in the receiving phase, possibly because participants are more focused on their own interests during that phase (Cappelletti et al. 2011). Through sufficient data collection, customized games will link age with social and cultural environments as well as gender, attempting to further analyze the influence of gender on the level of trust.

- The impact of social and cultural environments on trust between players in the trust game has been almost fully established. For example, Gelfand et al.'s research explored cultural differences in 62 societies and linked these differences to individuals' trust behavior in the trust game. The study found that cultural differences in individualism and collectivism significantly influence the level of trust between players in the trust game (Gelfand et al. 2004). In an individualistic cultural environment, people tend to exhibit more adventurous behavior, focusing more on individual interests and self-expression, which may result in more adventurous behavior. In a collectivist cultural environment, people place more emphasis on long-term interests and stable relationships, which may result in more conservative behavior (Gelfand et al. 2004). Therefore, before the game starts, customized games will ask players to briefly describe their own social and cultural environments as a reference for analyzing their behavior. Since social and cultural environments are a large category that cannot be comprehensively collected in a short period of time, this information is important but only serves as a reference.
oTree Experimental Code 


### Part 3:Spotlight

### Behavioral experimental paper：

Anderhub, Vital, Dirk Engelmann, and Werner Güth. "An experimental study of the repeated trust game with incomplete information." Journal of Economic Behavior & Organization 48, no. 2 (2002): 197-216.
(Anderhub et al. 2002)

- Research question: The main purpose of this paper is to study how participants' behavior develops in repeated trust games when they do not have complete information. Specifically, the researchers wanted to explore whether participants build trust over multiple rounds of the game, engage in more cooperative behavior, and whether their behavior is influenced by prior experience and backward induction when they do not know whether the other person will "betray" them (Anderhub et al. 2002).

- Difference from backward induction:Two different strategies were designed to explore how participants make decisions in repeated trust games. The first was a "psychological strategy," in which participants made decisions based on how much they trusted their opponents, and the second was a "social strategy," in which participants made decisions based on maximizing social benefits.Unlike backward induction, these strategies do not take into account what specific decisions an adversary might take, but simply consider decisions based on the participants' own trust and social interests. Backward induction is based on inferring the likely outcome of your opponent's actions in order to maximize your own gains.

- Behavioral foundation:The behaviour observed in the paper is based on participants' trusting and cooperative behaviour, as well as their expectations of future returns and attitudes towards risk. The results showed that participants' behavior was influenced by a number of factors, including their gender, cultural background, previous experience, information asymmetry, and the likelihood of repeated play. In addition, participants' behavior was influenced by psychological factors such as social norms, moral beliefs and concerns about fairness. Here is the basis for the behavior observed in several experiments:

1. Trust and return: Participants who invest in (fiduciaries) tend to reward trust by returning more money to investors later in the game.

2. Reputation: Participants build trustworthy or untrustworthy reputations based on their past actions in the game, which influence their behavior in subsequent rounds.

3. Conditional cooperation: Participants were more willing to cooperate (return more money) when they believed that another player was also likely to cooperate, and less likely to cooperate (return less money) when they believed that another player was likely to defect.


### Reinforcement learning paper:###
Wu, D. J., Steven O. Kimbrough, and Fang Zhong. "Artificial agents play the" Mad Mex trust game": a computational approach." In Proceedings of the 35th Annual Hawaii International Conference on System Sciences, pp. 389-398. IEEE, 2002.



### The game environment and learning algorithm:
The researchers designed a computer-simulated game environment called the "Mad Mex trust game"(We 2002). In the game, there are two agents, each with some coins. In each round, the agents can choose to cooperate or defect. If both agents choose to cooperate, they will each lose some coins but collectively gain more coins. If one agent chooses to defect, they will gain more coins, and the other agent will lose their coins. The goal of the agents is to maximize their total number of coins.
The researchers used a learning algorithm called Q-learning to train the agents. Q-learning is a feedback-based reinforcement learning algorithm in which the agents continually try and learn the optimal action strategy in the game to maximize their cumulative reward (We 2002). At the end of each round, the agents update their Q-value function to reflect the quality of the action they took. In the early stages of the game, the agents explore with random action strategies and adjust based on feedback. As the game progresses, the agents gradually develop more optimized strategies.

### Inspirations from reinforcement learning agent strategies:

The reinforcement learning agents in this paper adopted a cooperative strategy in the game. They are more inclined to choose cooperation rather than defection. This strategy has many similarities to the process of building trust between humans. For example, in human society, we generally tend to trust people who exhibit cooperation and honesty rather than those who exhibit betrayal and dishonesty.
By simulating this cooperative strategy, the reinforcement learning agents in this paper can gradually establish mutual trust in the game, which can be replicated and promoted in similar social situations. In addition, by analyzing the agents' strategy choices and learning processes, we can better understand the process of building trust between humans in social interactions and the psychological mechanisms of human decision-making. This knowledge can be applied to research and applications in social and economic fields, helping us better understand human behavior and design more effective policies and mechanisms to promote trust and cooperation.




### More about the Author

   
 ![image](WechatIMG46.png)
 
-  As a junior majoring in political economy, Rong Cong is very interested in economics, anthropology and psychology. She hopes to do enough cross-disciplinary research and study in the future. At the same time, Rong Cong is also a music lover. This is a cover of her song 👉🏻https://y.music.163.com/m/artist?app_version=8.9.61&id=46956986&userid=1572161264&dlt=0846.
   
### References

- Anderhub, Vital, Dirk Engelmann, and Werner Güth. "An experimental study of the repeated trust game with incomplete information." Journal of Economic Behavior & Organization 48, no. 2 (2002): 197-216.

- Aumann, Robert J. "Backward induction and common knowledge of rationality." Games and economic Behavior 8, no. 1 (1995): 6-19.

- Baron-Cohen, Simon, Rebecca C. Knickmeyer, and Matthew K. Belmonte. "Sex differences in the brain: implications for explaining autism." Science 310, no. 5749 (2005): 819-823.

- Berg, Joyce, John Dickhaut, and Kevin McCabe. "Trust, reciprocity, and social history." Games and economic behavior 10, no. 1 (1995): 122-142.

- Bohnet, Iris, and Richard Zeckhauser. "Trust, risk and betrayal." Journal of Economic Behavior & Organization 55, no. 4 (2004): 467-484.

- Bosson, Jennifer K., William B. Swann Jr, and James W. Pennebaker. "Stalking the perfect measure of implicit self-esteem: The blind men and the elephant revisited?." Journal of personality and social psychology 79, no. 4 (2000): 631.

- Cappelletti, Dominique, Werner Güth, and Matteo Ploner. "Being of two minds: Ultimatum offers under cognitive constraints." Journal of Economic Psychology 32, no. 6 (2011): 940-950.

- Charness, Gary, and Matthew Rabin. "Expressed preferences and behavior in experimental games." Games and economic behavior 53, no. 2 (2005): 151-169.

- Charness, Gary, and Matthew Rabin. "Understanding social preferences with simple tests." The quarterly journal of economics 117, no. 3 (2002): 817-869.

- Croson, Rachel, and Nancy Buchan. "Gender and culture: International experimental evidence from trust games." American Economic Review 89, no. 2 (1999): 386-391.

- Gelfand, M. J., D. P. S. Bhawuk, L. H. Nishii, D. J. Bechtold, R. J. House, P. J. Hanges, M. Javidan, P. W. Dorfman, and V. Gupta. "Culture, leadership, and organizations: The GLOBE study of 62 societies." Individualism and collectivism (2004): 437-512.

- McCabe, Kevin A., Mary L. Rigdon, and Vernon L. Smith. "Positive reciprocity and intentions in trust games." Journal of Economic Behavior & Organization 52, no. 2 (2003): 267-275.

- Sabbagh, Clara. "Joseph Henrich-Robert Boyd-Samuel Bowles-Colin Camerer-Ernst Fehr-Herbert Gintis (eds.): Foundations of Human Sociality: Economic Experiments and Ethnographic Evidence from Fifteen Small-Scale Societies." Sociologický časopis/Czech Sociological Review 44, no. 6 (2008): 1205-1207.

- Wu, D. J., Steven O. Kimbrough, and Fang Zhong. "Artificial agents play the" Mad Mex trust game": a computational approach." In Proceedings of the 35th Annual Hawaii International Conference on System Sciences, pp. 389-398. IEEE, 2002.


Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

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

