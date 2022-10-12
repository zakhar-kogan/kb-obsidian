- # Why network effects are critical
	- https://www.nfx.com/masterclass/network-effects/network-effects-mission-critical
	- Network effects (NE) may be the most important factor in predicting startup's success.
	- Between 2012 and 2018 70% of tech companies employed network effects.
	  collapsed:: true
		- ![image.png](../assets/image_1665553288535_0.png)
	- Viral effects are ==not== network effects. Network effect is *every user joining the product increases its value for all the other users*, Metcalfe effect.
- # The Underlying Properties Of Network Theory
	- https://www.nfx.com/masterclass/network-effects/network-theory-properties
	- ## Basic network
	  collapsed:: true
		- ![image.png](../assets/image_1665553803829_0.png)
	- ## Network density
	  collapsed:: true
		- ![image.png](../assets/image_1665553841794_0.png)
	- ## White hot center
	  collapsed:: true
		- So if there's one node where everybody's connecting to them, then you've got the beginnings of a **white hot center** with the core node, and then the nodes that are closest to them.
	- ## Directional / non-directional / bidirectional links
	  collapsed:: true
		- Another important aspect of these links is that they can be **directed**. There can be direction to these. So for instance, in Twitter, you would have an influencer who is important, sending out mostly messages to people who are just reading. That would be directional in one way. Or you could have, let's say a Venmo, where people are paying each other.
	- ## 1-1 / 1-many / many-many
	  collapsed:: true
		- ### Sarnoff's law
		  collapsed:: true
			- ![image.png](../assets/image_1665553956551_0.png)
			- Works for one-to-many
			- $V=n$
		- ### Metcalfe's law
		  collapsed:: true
			- ![image.png](../assets/image_1665554007062_0.png)
			- Works for many-to-many
			- $V=n^2$
		- ### Reed's law
		  collapsed:: true
			- ![image.png](../assets/image_1665554065662_0.png)
			- An improvement on Metcalfe's law by a MIT professor in 1999
			- Because of local clusters, the real value may grow as $V=2^n$
	- ## Critical mass
	  collapsed:: true
		- Or a point of inflection => **crucial** to start getting network effects.
		- So to build the network value, you need to get to critical mass. And what happens is, as your network is growing a little bit, a little bit, a little bit all the time, at some point, it hits a moment of critical mass where it takes off, it lifts off. You can feel it. It's like someone stuck two fingers in your nose and just yanks your head forward. It just starts to take off on its own. And that critical mass moment is often facilitated through **developing your clustering.**
		- Now to get these clusters going, you're going to want to find your **minimal viable cluster.** Some small group of people that once attached to each other will stay attached to each other that you can then build on. Again, maybe creating another cluster and then bridging those two clusters. That minimal viable cluster really helps you to found the overall network. Now, to get to critical mass, the product is going to have to have some value to these users, to this cluster.
		-
	- *Real > pseudonymous > anonymous* IDs
	- ## Homogeneity
	  collapsed:: true
		- ![image.png](../assets/image_1665554488688_0.png)
		- Conversely, **homogeneity** allows you to grow your network faster, but then often leaves you more vulnerable to attack by other competitors and other networks, simply because people are interchangeable. You think about Uber, you think about Lyft, you think about businesses where the needs are very clear and obvious, but it helps you grow faster at the beginning. So it's a trade off.
	- ## Asymptoting
	  collapsed:: true
		- Another interesting network property is what we call **asymptoting**. And asymptoting takes place when you might be adding more nodes onto the network, but the value doesn't actually continue to grow it. So the value of an Uber network or a Lyft network asymptotes even though you keep getting more drivers on the network, because if you're putting on your jacket or getting your bag, or you need to go to the bathroom before they come, you don't really care if they come faster than 4 minutes. It's nice if they come at 3 minutes, but as long as they come in under 10 or 6, it's pretty much good. And so the value doesn't actually get much higher.
	- ## Assymetry
	  collapsed:: true
		- So another important network property is what we call **asymmetry**.
		- In most marketplaces, **one side is harder** than the other. In some cases, much harder than the other. Example: Outdoorsy, doing an RV marketplace. They discovered that the supply side was much harder to get because there was, let's say, 2,500 mom and pops renting out about 50,000 RVs in the United States, but there was 30 million people trying to rent those RVs.
		- So if they could build software to allow them to work with and understand where these were, they would be able to *offer that supply out for the voracious demand* that was out there and build a pretty good marketplace, which they've done.
	- ## Cross-side network effect
	  collapsed:: true
		- ![image.png](../assets/image_1665554753592_0.png)
		- The two sides, in this case, are the supply and the demand. So the value is the more supply on the network, the more value to the demand side. So that's **cross-side network effect**, cross-side value being created, and that can be quite intense.
	- ## Negative network effects
	  collapsed:: true
		- ### Congestion
		  collapsed:: true
			- There's so many nodes on the network that are trying to use the network that the network starts to **break down**. A good example of that would be **Ethereum**, where the more people using Ethereum, the more the gas prices go up. It just becomes unaffordable to use that network.
		- ### Pollution
		  collapsed:: true
			- The **pollution** is when the nodes on the link are behaving badly. An example of behaving badly could be on Facebook when your grandmother gets on and she starts posting pictures of you as a kid and embarrassing you, you don't want to be on Facebook anymore.
	- ## Chicken egg problem
		- ![image.png](../assets/image_1665555056315_0.png)
		- Called **network start problem** for direct effect businesses. **Chicken and egg problem** for marketplaces.
		- You can't get anyone to join your network **unless there's already somebody there**.
		- *But how do you get them to sit there long enough? How do you attract them there at all? And then once you get them there, how do you attract enough of the demand so that these people stick around?* So there's a timing issue with bringing people in at the right time.
		- **Cold start problem** => the same situation, but when you've got a network, and there's **nobody there yet**. So when the first person comes in, there's no one there. How do you teach them to stick around so that they are there for their friends when their friends arrive?
	- ## Liquidity
	  collapsed:: true
		- *If someone lists something for sale on your marketplace, what percentage of the time do they sell it? What percentage of the time do they get the transaction they were looking for? If someone posts on your social network, what percentage of the time do they get likes, do they get attention, do they get responses, comments?* You can actually look at liquidity, both in terms of transactions on a marketplace and in terms of interaction on a network.
	- ## Multi-tenanting
	  collapsed:: true
		- So if you've got a supply and you've built your marketplace for the demand, they might be using your marketplace. But like with Lyft or Uber, I could sell my services on somebody else's marketplace, number two, or maybe marketplace number three. This happens if you're selling on eBay. You also want to sell on Amazon marketplace or on Shopify or on Etsy.
		- Can you build a system where either or both, the supply and the demand do not want to **multi-tenant** so you can capture their share of wallet, capture their average order value, capture the overall annual take that you're going to be taking from them? That's one thing you need to think about when designing your marketplace is how to keep them from multi-tenanting.
	- ## Related concepts
		- ### Viral effects
			- **Viral effects** are awarding your existing users get you new users for free. There are playbooks for that and that's great, but that's not what we're talking about. Network effects are about retention. Network effects are about defensibility. And the defensibility is what ultimately adds value to your part.
			- ![image.png](../assets/image_1665555627291_0.png)
			- $K=\frac {Interactions*Conversion}{time}$
			- Now, if you get a *K-factor of 1.01* for many days in a row, you will eventually start growing very geometrically. And if you can get a viral factor of 1.25, back in the day, maybe 10 or 15 years ago, it was possible to get viral factors as high as 3.0, meaning you would triple every day. And in many cases, we were registering 250,000 people a day.
			- I know of one application that was registering 2 million people a day on top of the Facebook platform. Because there was no viral delay, the invites were going out like crazy. And the conversion rate was really high because people were already on Facebook.
			- Those conditions don't exist today anymore. But understanding viral effects, understanding virality, how to measure your *K-factor can be useful to lowering your CAC* today.
		- ### Linear vs geometric growth
		  collapsed:: true
			- ![image.png](../assets/image_1665555592998_0.png)
-