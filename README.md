>phd about trust
https://perso.liris.cnrs.fr/omar.hasan/publications/hasan_2010_thesis.pdf

>https://hal.archives-ouvertes.fr/hal-01635314/document


Various inputs are used by social trust algorithms to measure the trustworthiness of agents. In EigenTrust [1], PeerTrust [2], TRAVOS [6] and Beta Reputation System (BRS) [7], agents rate their satisfaction after a transaction (e.g., downloading a file in a P2P file-sharing network). These ratings are used to obtain a trust score that represents the
trustworthiness of the agent.


<img src="/pictures/84.PNG" width="500px">

https://eudl.eu/pdf/10.4108/icst.collaboratecom.2011.247125


## Trust model types
<img src="/pictures/77.PNG" width="500px">

https://www.oasis-open.org/committees/download.php/28303/JIB2007-DSS-Survey.pdf
<img src="/pictures/79.PNG" width="500px">
In most cases, the calculation of trust
was based on the similarity of users in selecting items or their neighbors. The use of this type of trust may not be
significantly accurate in making recommendations since only behavioral similarity, or neighborship cannot be a
reliable factor in creating trust and the user that is considered as a trusted user may not be highly ranked in the
social network (have few friends) and may not be a known and famous person, and this issue causes distrust.

## Algorithms
Many systems focused  on  developing  trust  and  reputation systems<br>

- **EigenTrust**  is  one  of  the  most  popular  reputation  algorithms  used  in  P2P  networks;  this algorithm  uses  an  eigenvector in its  calculation  of  a  trust  value.  The EigenTrust reputation management system is among
the most known and successful reputation systems. **On the other hand, a main drawback of this system
is its reliance on a set of pre-trusted peers which causes nodes to center around them. As a consequence,
other peers are ranked low despite being honest, marginalizing their effect in the system**.As a consequence, other peers would be ranked low despite
potentially being honest (Chiluka et al., 2012), marginalizing their role in deciding reputations of other peers and limiting
their chances of being chosen as download sources even though they have files of better quality than pre-trusted peers.
Furthermore, if a pre-trusted peer downloads an inauthentic file from a malicious peer, this would allow the file to be easily accepted by other peers, leading to a chain of inauthentic downloads.<br>

*local trust in EigenTrust* *𝑠𝑖𝑗=𝑠𝑎𝑡(𝑖,𝑗)−𝑢𝑛𝑠𝑎𝑡(𝑖,𝑗)* is  defined  as  local  trust  value between  two  peers  i  and  j,  where  sat(i,j)  is  the  number  of  satisfactory  transactions  and *unsat(i,j)*  is  the  number  of  unsatisfactory  transactions  between  peers  i  and  j
Then we normlize the values == a node devide the 
These  local trust  values  have  unlimted  domain,  and  they  can  also  be  negative.  Eigen  Trust  demands them  to  be  normalized  to  values  between  0  and  1.  Normalized  values  of  trust  between nodes i and j aregiven by this equation
 ![](/pictures/25.PNG)(max s,0 as can be -)
Where *𝑠𝑖𝑗* is the local trust value and 𝑐𝑖𝑗 is thenormalized local trust value between nodes iandj.  We  can  see  from  the  expression  that  all  trust  values  are  from interval  [0,1]
Note that we cannot use sij as the local trust score without normalizing, because malicious agents can arbitrarily assign high local trust values to fellow malicious agents and
low local trust values to honest agents.
![](/pictures/30.PNG)
 <br>
![](/pictures/24.PNG)
![](/pictures/82.PNG)
- **HonestPeer (2015)** extends the original EigenTrust algorithm to overcome the issue of peers congregating around pre-trusted peers [Kurdi (2015)]. HonestPeer selects the most reputable (i.e.,honest) peers dynamically based on the quality of the files each peer provides. enhancing the EigenTrust algorithm by giving peers with high reputation values (honest peers) a role in calculating the global reputation of other peers. Rather than solely depending on the static group of pre-trusted peers, the proposed algorithm, HonestPeer, selects the
most reputable nodes, honest peers, dynamically based on the quality of the provided files. It aims at giving peers with high reputation values a role in calculating the reputation of other peers
- Another trust-based algorithm, **PeerTrust**, calculates trust based on several factors such as feedback, number of transactions, credibility and community context factors[Xiong and Liu (2004)]. Alternatively, algorithms such as GroupTrust organise peers into different groups based on their evaluation of the same or similar services [Zhang, Zheng, Liu et al. (2011)]. In these instances, the evaluation of the trustworthiness of peers outside the group is based on their local and global reputations, which are aggregated from other peers.  The PeerTrust reputation management system proposed in Xiong and Liu (2004), computes the peer reputation as the average trust values weighted by the score of peers providing these values, the number of transactions in which they were involved and the credibility of their feedback, among other
factors. The main drawback of this approach is the heavy overhead associated with retrieving weighting factors (Hwang
et al., 2012).
In developing HonestPeer, the **five design objectives of reputation systems identified by EigenTrust (Kamvar et al., 2003) were considered**<br>
![](/pictures/29.PNG)
- **TrustFeer** is  another trust management system  proposed  for P2P federated clouds [Kurdi,  Alshayban,  Altoaimy  et  al.  (2018)].  The  algorithm  relies  on  subjective  logic opinionsthat are based on the reputation of peersand on service level agreements (SLAs) when evaluating the trustworthiness of peers.<br>
- **HierarchTrust**, a novel trust model that relies on the standard deviation in its trust calculations. HierarchTrust determines trust based on values assigned to various factors, including trust, reputation, feedback and recommendations, which are checked in order  of  their reliability  as  measures  of trust.

- In (Zhou and Hwang, 2007), the **PowerTrust** reputation system developed dynamically selects a small number of nodes that are most reputable, using a distributed ranking mechanism. These nodes are called Power Nodes and play an important role in calculating the global and local reputation values of other peers. By using a look-ahead random walk strategy and leveraging the power nodes, PowerTrust is known for its ability to improve the global reputation accuracy and the trust values aggregation speed. On the other hand, it takes time until power nodes are selected and identified

## SecTrust paper
![](/pictures/87.PNG)

## Policy based vs. Reputation based Trust Management 
The term trust management, introduced in [5] as “a unified approach to specifying and interpreting security policies, credentials, and relationships which allow direct authorization of security-critical actions”, has been given later a broader definition, not limited to authorizations [12]: “Trust management is the activity of collecting, encoding, analyzing and presenting evidence relating to competence, honesty, security or dependability with the purpose of making assessments and decisions regarding trust relationships”. Two main approaches are currently available for managing trust: policy-based and reputation-based trust management.
The focus here is on trust computation models capable of estimating the degree of trust that can be invested in a certain party based on the history of its past behavior. The main issues characterizing the reputation systems are the trust metric (how to model and compute the trust) and the management of reputation data (how to securely and efficiently retrieve the data required by the trust computation) [3].
Typically, reputation-based trust is used in distributed networks where a system only has a limited view of the information in the whole network. New trust relationships are inferred based on the available information (following the idea of exploiting the world's information). In these scenarios, the available information is based on the recommendations and the experiences of other users, and it is typically not signed by certification authorities but (possibly) self-signed by the source of the statement. This approach supports trust estimates with a wide, continuum range and allows the propagation of trust (e.g., transitive propagation) along the network as well as weighting of values (e.g., fresher information vs. older information).


## Metrics
**Feedback in Terms of Amount of Satisfaction**. Reputation-based systems rely on feedback to evaluate a peer. Feedback in terms of amount of satisfaction a peer receives during a transaction reflects how well this peer has fulfilledits part of the service agreement. Some existing reputationbased systems use this factor alone and compute a peer u’s trust value by a summation of all the feedback u receives through its transactions with other peers in the community. For example, buyers and sellers in eBay can rate each other after each transaction (+1, 0, -1) and the overall reputation is the sum of these ratings over the last six months. We can clearly see that these feedback-only metrics are flawed. A peer who has performed dozens of transactions and cheated one out of every four cases will have a steadily rising reputation in a given time duration whereas a peer who has only performed 10 transactions during the given time duration, but has been completely honest, will be treated as less reputable if the reputation measures of peers are
computed by a simple sum of the feedback they receive. Dellarocas[11] concluded that binary reputationmechanisms will not function well and the resulting market outcome will be unfair if judgment is inferred from knowledge of the sum of positive and negative ratings alone.<br>
**Number of Transactions**. As described above, a peer may increase its trust value by increasing its transaction volume to hide the fact that it frequently misbehaves at a certain rate when a simple summation of feedback is used to model the trustworthiness of peers.
The number of transactions is an important scope factor for comparing the feedback in terms of degree of satisfaction among different peers. An updated metric can be defined as the ratio of the total amount of satisfaction peer u receives over the total number of transactions peer u has, i.e., the average amount
of satisfaction peer u receives for each transaction
<br>
**Social trust model** should provide a means to compare the trustworthiness of agents in order to choose a
particular agent to perform an action. For instance, on an e-commerce website like eBay, we need to be able to compare the trustworthiness of sellers in order to pick the most
trustworthy one to buy a product from. Social trust models rely on past experiences of agents to produce trust assertions. That
is, the agents in the system interact with each other and record their experiences, which are then used to determine whether a particular agent is trustworth
## Issues
issues:
- Collusion — Shilling Attack, where malicious nodes submit dishonest feedback and collude with each other to boost their own ratings or bad-mouth non-malicious nodes
- Reputation Cashing — Agents cashing in on their good reputation to carry fraudulent transactions with higher gain
- Strategic Deception — Establishing initial trust for new agents more dynamically (using reputation on other networks, feedback from agents that they have transacted with)
- Faking Identity — Agents faking identities within social impact networks to steal disbursed, charitable resources

### Security 
self-promotion and slandering.
1. Bad-mouthing attack is to provide dishonest recommendations to deframe
good nodes, which is the most straightforward attack [21]. In our protocol,
malicious nodes can continuously give bad comments to a specific node or all
other nodes to improve his trustworthiness ranking in a block in return.
2. Replay attack attempts to reuse transactions and replay them in order to
increase the impact of the same transaction. By carrying out this attack, a
malicious participant can claim he has been involved in a transaction that is
profitable for him multiple times. It can also be used to undermine hostile
participants.
3. On-off attack is referred to irregular behaviors of attackers, which means
that malicious nodes can perform well or badly alternatively in order to
remain undetected while causing damage.
4. Sybil attack and newcomer attack, which was first described by Douceur
[22], is harmful to almost all p2p networks. It can be described that attackers
“legally” create more than a single ID. If one ID gets low reputation by
performing bad behaviors, it switches to a new ID and starts over
### tools
<img src="/pictures/83.PNG"> https://www.hindawi.com/journals/wcmc/2018/1073216/tab1/
# Overview of reputation systems
List of available reputation systems and aggregation algorithms

|  Year | Short name | Full Paper title |
|  ------ | ------ | ------ |
|  Research |  |  |
|  2000 | [Histos](https://ac.els-cdn.com/S0167923600000841/1-s2.0-S0167923600000841-main.pdf?_tid=spdf-3c6ff25f-0718-4665-8559-4643540a6d4b&acdnat=1519309632_fda7f44a98400ea7f4e08923e47d21c1) | Collaborative reputation mechanisms for electronic marketplaces |
|  2000 | [Sporas](https://ac.els-cdn.com/S0167923600000841/1-s2.0-S0167923600000841-main.pdf?_tid=spdf-3c6ff25f-0718-4665-8559-4643540a6d4b&acdnat=1519309632_fda7f44a98400ea7f4e08923e47d21c1) | Collaborative reputation mechanisms for electronic marketplaces |
|  2001 | [Regret](http://delivery.acm.org/10.1145/380000/376110/p194-sabater.pdf) | REGRET: reputation in gregarious societies |
|  2001 | [P-Grid](http://delivery.acm.org/10.1145/510000/502638/p310-aberer.pdf?ip=145.94.192.53&id=502638&acc=ACTIVE%20SERVICE&key=0C390721DC3021FF%2E512956D6C5F075DE%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1519310215_62eb641df69cd44807ec3bf5a119974d) | P-Grid: a self-organizing structured P2P system |
|  2002 | [Beta](https://domino.fov.uni-mb.si/proceedings.nsf/proceedings/d9e48b66f32a7dffc1256e9f00355b37/$file/josang.pdf) | The Beta Reputation System |
|  2002 | [Confidant](https://dl.acm.org/citation.cfm?id=513828) | Performance analysis of the CONFIDANT protocol |
|  2002 | [XRep](https://dl.acm.org/citation.cfm?doid=586110.586138) | A reputation-based approach for choosing reliable resources in peer-to-peer networks |
|  2003 | [EigenTrust](https://dl.acm.org/citation.cfm?doid=775152.775242) | The Eigentrust algorithm for reputation management in P2P networks |
|  2003 | [Gupta et al.](https://dl.acm.org/citation.cfm?doid=776322.776346) | A reputation system for peer-to-peer networks |
|  2003 | [TrustMe](http://www.ida.liu.se/conferences/p2p/p2p2003/presentations/TrustMe-prez.pdf) | TrustMe: anonymous management of trust relationships in decentralized P2P systems |
|  2003 | [PeerTrust](https://www.cse.iitb.ac.in/~madhumita/trust/xiong03peertrust.pdf) | PeerTrust: supporting reputation-based trust for peer-to-peer electronic communities |
|  2004 | [Ismail et al.](http://sefcom.asu.edu/publications/group-hierarchies-constrained-iceis2004.pdf#page=64) | An Efficient Off-Line Reputation Scheme Using Articulated Certificates |
|  2004 | [Pride](https://dl.acm.org/citation.cfm?doid=1013367.1013535) | Pride: peer-to-peer reputation infrastructure for decentralized environments |
|  2005 | [TrustGuard](https://dl.acm.org/citation.cfm?doid=1060745.1060808) | TrustGuard: countering vulnerabilities in reputation management for decentralized overlay networks |
|  2005 | [FuzzyTrust](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1541943) | Trusted P2P Transactions with Fuzzy Reputation Aggregation |
|  2005 | [Travos](https://eprints.soton.ac.uk/260581/2/Patel2005.pdf) | A Probabilistic Trust Model for Handling Inaccurate Reputation Sources |
|  2007 | [PowerTrust](http://gridsec.usc.edu/files/publications/tpds-0463-1105.r2-final-june21.pdf) | PowerTrust: A Robust and Scalable Reputation System for Trusted Peer-to-Peer Computing |
|  2008 | [Gal-Oz et al.](https://link.springer.com/content/pdf/10.1007/978-0-387-09428-1_11.pdf) | A Robust and Knot-Aware Trust-Based Reputation Model |
|  2009 | [Conner et al.](https://dl.acm.org/citation.cfm?doid=1526709.1526829) | A trust management framework for service-oriented environments |
|  2009 | [H-Trust](https://link.springer.com/content/pdf/10.1007/s11390-009-9275-7.pdf) | H-Trust: A Group Trust Management System for Peer-to-Peer Desktop Grid |
|  2009 | [RateWeb](https://link.springer.com/content/pdf/10.1007/s00778-009-0138-1.pdf) | RATEWeb: Reputation Assessment for Trust Establishment among Web services |
|  2009 | [Tong and Zhang](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5366961) | Group Trust and Group Reputation |
|  2010 | [DHTrust](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5683742) | DHTrust: A Robust and Distributed Reputation System for Trusted Peer-to-Peer Networks |
|  2011 | [R2Trust](https://ac.els-cdn.com/S0167739X11000343/1-s2.0-S0167739X11000343-main.pdf?_tid=1a46dd30-17e0-11e8-8edf-00000aab0f27&acdnat=1519311371_9be633e42c502d21ac63e6e6d3ca911f) | R2Trust, a reputation and risk based trust management framework for large-scale, fully decentralized overlay networks |
|  2014 | [ReDS](https://arxiv.org/pdf/1209.4867.pdf) | ReDS: A Framework for Reputation-Enhanced DHTs |
|  2013 | [Tulungan](http://sdiwc.net/digital-library/request.php?article=79498f986833e6ca70577a286a2b584e) | TULUNGAN: A SELF-PROMOTING-RESISTANT REPUTATION SYSTEM FOR COLLABORATIVE WEB FILTERING SYSTEMS |
|  2013 | [GRAft](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6683929) | Policy Derived Access Rights in the Social Cloud |
|  2014 | [PerContRep](https://link.springer.com/content/pdf/10.1007%2Fs11227-014-1116-y.pdf) | PerContRep: a practical reputation system for pervasive content services |
