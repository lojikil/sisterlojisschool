# Sister Loji's Modeling School for Wayward InfoSec Youth
## meditations on applying various infosec models
### and giving your best blue steel

_16DEC2020, Mid-Winter's Night Con_

---

# Take aways

1. this talk focuses on four domains we can model (risk, threat, maturity, and (semi-)formal)
1. from a  data-centered, control-centered position
1. with a focus on practical techniques

_do you or someone you know suffer from the following:_

- inability to understand your infosec programs?
- anxiety or concern about the state of your systems?
- feels of despair or loss of control as to where your data ends up?

> Sister Loji's Modeling School for Wayward InfoSec Youth is an absurdist-focused 
> school meant to help youth  from all walks of life better model & understand their
> infosec programs

---

# outline

1. intros
1. what is modeling?
1. why model?
1. what are we modeling?
   1. practical techniques for the wayward youth
   1. risk
   1. threat
   1. maturity
   1. (semi-)formal
1. what do we get out of modeling?
1. Lifting vs Extraction
1. Application

---

# `$ finger lojikil`

```
[lojikil.com]
Stefan Edwards (lojikil) is not presently logged in.

- Practice Lead at Trail of Bits
- Twitter/Github/Lobste.rs: lojikil
- Works in: Defense, FinTech, Blockchain, IoT, compilers,
vCISO services, threat modeling
- Previous: net, web, adversary sim, &c. 
- Infosec philosopher, programming 
language theorist, everyday agronomer, father.
- As heard on Absolute AppSec (multiple) and Risky
Business (No. 559).

WARNING: DEAF
WARNING: Noo Yawk
```

---

# Trail of Bits

- large number of smart contract assessments (5-10 *per month*)
- large number of bespoke blockchain assessments (~ 5 *per year*)
- work in large code bases like Kubernetes, etcd, &c.
- work in fundamental program analysis research for DARPA
- work on tools like Manticore (symbex), Echidna (property testing), Slither (static analysis & absint)
- surrounding areas: cryptography, infra, &c

_publications: github.com/trailofbits/publications_

---

# what is modeling?

I like [Wikipedia's](https://en.wikipedia.org/wiki/Modeling_language) definition:

> A modeling language is any artificial language that can be used to express information
> or knowledge or systems in a structure that is defined by a consistent set of rules.
> **The rules are used for interpretation of the meaning of components in the structure.**

- basically, break down things in a consistent way
- express information in a consistent fashion
- to help us understand meaning

---

# what is modeling?

<!--
so really we do this all the time...
-->

- we make models all the time
- drawings
- data flows
- simple comments
- this talk is meant  to  help _formalize_ those
- take you from this: `NOTE: balance should be great than withdrawl before execution`
- to this:

```
// @assignable balance
// @requires balance >= 100
// @requires withdrawal <= balance
// @ensures balance == \old(balance) - withdrawal
```

---

# why model?

- let's look at that example
- original: `NOTE: balance should be great than withdrawl before execution`
    1. mispelt "withdrawal?" "greater than?"
    1. what does "should be mean?"
    1. what's the result of all of this?
- new:
    1. the system checks our spelling
    1. we know that `balance` is modified
    1. we know that balance must be greater than or equal to 100
    1. we know that the withdrawal amount must be less than or equal to the balance
    1. and we know the result is equal to the original balance less the withdrawal
    1. all enforced by our modeling language
- result: better design, more understanding

---

# why model?

<!--
I think very often we get stuck on what "modeling" actually means; we want some sort
of output from modeling, not really realizing that models are just code/data that we
can further manipulate to our needs 
-->

- there are infinite output types
  - process diagrams
  - simple box visualizations
  - user process diagrams
  - code extraction
  - assertions
- work with your teams & orgs to best fit what you need to use
- models, esp models as code, should be updated, manipulated, re-run with new constraints
  - stop thinking in terms of model car
  - start thinking in terms of simulation & modeling

---

# why model?

.left[![user-centric data flow](img/designbycontract.png)]
.right[![a simple request diagram](img/dataflow0.png)]

---

# why model?

<!--

This was a huge system with numerous components, but the other interesting thing was that 
sitting down and modeling the data flow really helped with the general understanding of
the  system for everyone involved. We then used this to drive where our risks were

-->

![the Voatz arch would have been impossible to approach without some form of model](img/Arch-Draft-v9_public_attacker.png)

---

# why model?

- honestly? a secret: bang for buck, threat modeling often finds more bugs than risk modeling in terms of effort
- folks reconsider designs, choices, and so on just by talking it out
- in terms of density, 8-10 findings falling out from a 30-60 minute call isn't unusual
- simplifies down the system under test
- model our thoughts there

![that's my secret](img/thatsmysecret.png)

---

# what are we modeling?

## four things we should model (in decreasing order)

- risk: a measure of impact ([ala NIST's definition](https://csrc.nist.gov/glossary/term/risk))
  - likelihood x impact = system severity
  - system severity x importance of data = organizantional severity
  - tied to things like reputation, financial loss, regulatory loss, &c
  - see NIST 800-30, 37, 39, ISO 27k1, &c.
- threat: the potential for impact ([again via NIST](https://csrc.nist.gov/glossary/term/threat))
  - what can an actor do with your system?
  - what controls are in place to stop that?
  - what data do they have access to?
- maturity: the robustness of processes & controls
  - how robust are the tools and processes the team uses?
  - where are they located?
  - how documented are they?
  - see NIST CSF, PRISMA, &c.
- (semi-)formal: mathematical/logical models of processes of a system's flow
  - way too many things for one talk
  - we'll focus on design by contract
- often, we're missing all but the first (and sometimes the first)

---

# what are we modeling? risk

---


# what are we modeling? threat

---

# what are we modeling? maturity

---

# an aside: maturity vs posture

---

# what are we modeling? (semi-)formal/correctness

---

# what do we get?

---

# Lifting  vs Extraction

---

# Application

---

# Outro
