- title: The Pseudonymous Bridge
- authors: Lev Soukhanov and Yaroslav Rebenko
- Прочитать
	- Perfect zero-[[knowledge]] in random oracle model
		- Intuitively, it should capture the property that **the proof does not reveal any useful information about the private value y.**
	- Fiat-Shamir transformation
	- [[vector]] Schnorr proofs
	- PoA blockchain https://en.wikipedia.org/wiki/Proof_of_authority
	  id:: 62f93f2d-584e-4db8-9a82-a39ba7f28730
- Конспект
	- The anonymity set is the set of all relatively active users of the [[Network]] (publishing at least **one public message in a validation epoch**).
	- In practice, there is no [[crypto]]-twitter. However, as we show, it is actually not needed: a bit more elaborate protocol allows to create a pseudonymous bridge from any public [[social]] [[Network]], without permission. We [[stress]] that it also does not require steganography or even publishing of any cryptographic data in this public [[social]] [[Network]], and the anonymity set is the set of all relatively active users of the [[Network]].
	- The second problem is private contact search. This is a typical problem for privacy-focused messenger applications: for example, [[signal]] does not [[learn]] anything about user’s contact list, but it needs to expose their phone number to everyone. This is also a core issue preventing us from creation of scalable [[decentralized]] webs of trust.
	- The standard Schnorr proof for a pair of points A, B ∈ E is a proof of [[knowledge]] of λ ∈ Zq such that λA = B.
	- Practically, it can be implemented as a [[Network]] of nodes using **Dandellion++ protocol,** combined with a simple ((62f93f2d-584e-4db8-9a82-a39ba7f28730))
	- ### Public [[Network]] oracle
	  This is an entity which periodically publishes the Merkle root of all messages in twitter (with subtrees corresponding to individual accounts).
	- ### Salt workers
	  This is a set of special participants which indulge in a simple [[MPC]] protocol. Let us fix an elliptic [[Curve]] E of prime order q such that DDH assumption is hard in it. Each salt worker i keeps a secret parameter λi ∈ Zq. Honest salt workers do not share their parameters with anyone.
	- Naive approach to the problem would be forming some commitment to a future message m (here and after, we assume that messages include some metadata, at least the sending user and timestamp). *However, if this commitment is hiding (say, Hash(m|r)), where r is some random string, one could commit to the same message twice and register two accounts. If the commitment would be linkable (say, Hash(m)), then an adversary could post-factum calculate hashes of all new messages in public [[social]] [[Network]], and check whether a user have registered or not.*
	- Both of these problems can be solved if one makes the result of salting consistent between epochs. But that comes at a cost.
	  Main change is, instead of choosing λi ’s independently, salt workers now use Shamir’s secret sharing. *In case the salt worker set changes, key redistribution is necessary.*
-