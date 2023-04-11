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

The Trust game is an experiment aimed at studying human trust and cooperative behavior. In this game, there are two participants: investor A and receiver B. Investor A has a certain amount of money and can choose to give some of it to receiver B. This money will be doubled, and receiver B can choose to return some of it to investor A or keep all the money. If receiver B chooses to return some of the money to investor A, then both investor A and receiver B will jointly receive more money. However, if receiver B chooses to keep all the money, then investor A will lose their investment. Analyzing the behavior of the investor and receiver can effectively analyze the psychology of human trust and cooperative behavior in real life.

- Game Environment:


### Code

The customized game changed three things from the original game. First, the endowment went from 100 to 10,000. Second, the multiplier went from 3 to 10,000. Third, custom games collect the gender and age of the player and the socio-cultural environment of the simple player before the game starts.I will introduce the reasons for my modification in detail below.

### Explanation

- Traditional research suggests that in general, the more initial endowment, the more likely Player A is to choose to share, while Player B is more likely to share some or all of their endowment with Player A (Charness et al. 2005). This is because the amount of initial endowment affects Player A's expected earnings and risk perception. If the endowment is high, Player A will be more likely to bear the risk of sharing and will have more confidence in obtaining higher returns. For Player B, the amount of endowment also affects their expected earnings and risk perception. If the endowment is high, they will be more likely to share because they believe in Player A's sharing behavior and higher returns (McCabe et al. 2003). In the customized game, the initial endowment is set at $10,000, a relatively considerable amount. In estimating and assuming the game results, Player A is expected to share at least some of their endowment with Player B. This makes any choice not to share the initial endowment very interesting and worth studying.

- Berg, Dickhaut, and McCabe's classic study found that the higher the multiplier, the higher the sharing rate of players in the trust game (Berg et al. 1995). At the same time, Bohnet and Zeckhauser's research also found that a high multiplier can increase trust and returns, thereby reducing untrustworthy behavior (Bohnet et al. 2004). Based on these studies, the multiplier in the new trust game will reach 10,000. This means that the potential benefits of choosing to trust the other player will become incredibly huge, and any small changes in the sharing of funds will bring about huge changes in the results. The customized game hopes to see how much risk people are willing to take under infinite temptation.

- Gender is expected to affect the level of trust between players in the trust game. First, there are some differences between men and women in terms of socialization, which may affect their behavior in the trust game. For example, some studies have shown that women's brains are more adaptable to social and emotional stimuli, while men's brains are more adaptable to spatial and motion stimuli (Baron-Cohen et al. 2005). Women pay more attention to the intimacy of interpersonal relationships, so they attach more importance to the trust and care of the other party, while men tend to seek greater returns through adventure (Baron-Cohen et al. 2005). Secondly, societal expectations of men and women may also affect their behavior in the trust game. For example, some studies have shown that society tends to view men as more confident and adventurous, so men may be more inclined to take risks in the trust game (Bosson et al. 2000). However, other studies have pointed out that there are differences in the behavior of men and women from different cultural backgrounds in the trust game, but gender itself does not have a significant impact on trust behavior (Croson et al. 1999). Therefore, whether gender affects players' choices is one of the factors that the game hopes to analyze through sufficient data collection.

- Age is expected to influence the level of trust between players in the trust game. Participants who are older tend to exhibit higher levels of trust in the trust game, which may be related to a more stable and conservative mindset that develops with age (Cappelletti et al. 2011). However, some experiments have shown that age does not significantly affect behavior in the receiving phase, possibly because participants are more focused on their own interests during that phase (Cappelletti et al. 2011). Through sufficient data collection, customized games will link age with social and cultural environments as well as gender, attempting to further analyze the influence of gender on the level of trust.

- The impact of social and cultural environments on trust between players in the trust game has been almost fully established. For example, Gelfand et al.'s research explored cultural differences in 62 societies and linked these differences to individuals' trust behavior in the trust game. The study found that cultural differences in individualism and collectivism significantly influence the level of trust between players in the trust game (Gelfand et al. 2004). In an individualistic cultural environment, people tend to exhibit more adventurous behavior, focusing more on individual interests and self-expression, which may result in more adventurous behavior. In a collectivist cultural environment, people place more emphasis on long-term interests and stable relationships, which may result in more conservative behavior (Gelfand et al. 2004). Therefore, before the game starts, customized games will ask players to briefly describe their own social and cultural environments as a reference for analyzing their behavior. Since social and cultural environments are a large category that cannot be comprehensively collected in a short period of time, this information is important but only serves as a reference.
oTree Experimental Code 


### Spotlight
- Behavioral experimental paper：Fowler, James H., and Nicholas A. Christakis. "Cooperative behavior cascades in human social networks." Proceedings of the National Academy of Sciences 107, no. 12 (2010): 5334-5338.

What research question does the behavioral experimental research intended to address?

The behavioral experiment was designed to explore non-economic considerations of trust behavior, such as emotional and social factors, and how these affect how people behave in trust games. Specifically, the authors focus on three research questions: 
i. Do people take into account each other's emotional states during trust games? 
ii.  Are people affected by social factors in the trust game? 
iii.  What are the effects of these non-economic factors on people's trust behavior?

### More about the Author

   
 ![image](WechatIMG46.png)
 
-  As a junior majoring in political economy, Rong Cong is very interested in economics, anthropology and psychology. She hopes to do enough cross-disciplinary research and study in the future. At the same time, Rong Cong is also a music lover. This is a cover of her song 👉🏻https://y.music.163.com/m/artist?app_version=8.9.61&id=46956986&userid=1572161264&dlt=0846.
   
### References

- Baron-Cohen, Simon, Rebecca C. Knickmeyer, and Matthew K. Belmonte. "Sex differences in the brain: implications for explaining autism." Science 310, no. 5749 (2005): 819-823.

- Berg, Joyce, John Dickhaut, and Kevin McCabe. "Trust, reciprocity, and social history." Games and economic behavior 10, no. 1 (1995): 122-142.

- Bohnet, Iris, and Richard Zeckhauser. "Trust, risk and betrayal." Journal of Economic Behavior & Organization 55, no. 4 (2004): 467-484.

- Bosson, Jennifer K., William B. Swann Jr, and James W. Pennebaker. "Stalking the perfect measure of implicit self-esteem: The blind men and the elephant revisited?." Journal of personality and social psychology 79, no. 4 (2000): 631.

- Cappelletti, Dominique, Werner Güth, and Matteo Ploner. "Being of two minds: Ultimatum offers under cognitive constraints." Journal of Economic Psychology 32, no. 6 (2011): 940-950.

- Charness, Gary, and Matthew Rabin. "Expressed preferences and behavior in experimental games." Games and economic behavior 53, no. 2 (2005): 151-169.

- Croson, Rachel, and Nancy Buchan. "Gender and culture: International experimental evidence from trust games." American Economic Review 89, no. 2 (1999): 386-391.

- Gelfand, M. J., D. P. S. Bhawuk, L. H. Nishii, D. J. Bechtold, R. J. House, P. J. Hanges, M. Javidan, P. W. Dorfman, and V. Gupta. "Culture, leadership, and organizations: The GLOBE study of 62 societies." Individualism and collectivism (2004): 437-512.

- McCabe, Kevin A., Mary L. Rigdon, and Vernon L. Smith. "Positive reciprocity and intentions in trust games." Journal of Economic Behavior & Organization 52, no. 2 (2003): 267-275.

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

