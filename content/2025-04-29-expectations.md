# Expectations and General Thoughts
Throughout these reflective pieces, I shall use Gibbs' Reflective Cycle as a framework for structuring my thoughts on my experiences in this module, what I feel I have learned and how I plan to apply it. This model follows 6 stages:
- Description of the experience
- Feelings and thoughts about the experience
- Evaluation of the experience, both good and bad
- Analysis to make sense of the situation
- Conclusion about what you learned and what you could have done differently
- Action plan for how you would deal with similar situations in the future, or general changes you might find appropriate.
(The University of Edinburgh, 2024)

My career as a software engineer has focussed mostly on producing safety-critical software for systems such as train control systems. While this has taught me a great deal about the considerations that must be made in order to ensure your software runs without problem, it has not given me much insight into developing secure applications from a security perspective.

I was therefore excited to gain new perspectives in a domain that, so far, has eluded me. Although my main experience to date has been safety-critical, using languages such as Ada and its subset SPARK to craft software that is error-free, I believe there is a wide overlap between this and the world of security focussed development. The aim of both is to ensure the software remains doing what it was designed to do, albeit with different threats to protect from. In safety-critical we are protecting against programming errors by using languages which come with baked-in guarantees about how they will execute based on formal proofs. 

## Reflection
What I have found during this module is that much of secure software development is the same. For example, encryption algorithms such as Advanced Encryption Standard (AES) that would take a supercomputer 1 billion billion years on average to brute force (Arora, 2012). The methods that are employed in order to protect against security vulnerabilities share a common theme with those languages I have used, both rely on maths to underpin their proofs. The security of an encryption algorithm can simply lie in how long, on average, it would take to crack it.

Of course, there's more to these algorithms than purely the formal proofs that form them. For example, users must send and receive cryptographic material to verify they are who they say they are and precautions must be taken to ensure this does not fall into the hands of attackers. Nothing demonstrated this better than the coding assignment in Unit 11. This helped solidify the principle that, even with the use of encryption libraries, if user data is not processed in a safe way the benefits it brings can be nullified.

# References
Arora, M. (2012) _How Secure is AES 128 and 256 Encryption Against Brute Force Attacks?_. Available at: https://www.eetimes.com/how-secure-is-aes-against-brute-force-attacks/ (Accessed 8 June 2025).

The University of Edinburgh. (2024) *Gibbs' Reflective Cycle*. Available at: https://reflection.ed.ac.uk/reflectors-toolkit/reflecting-on-experience/gibbs-reflective-cycle (Accessed: 16 July 2025).