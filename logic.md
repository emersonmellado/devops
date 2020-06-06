# INTRODUCTION to LOGIC

## Why study Logic?

Computers are ~~dumb~~ machines, they are basically thousands of light switches turning itself on or off according to whatever we tell them to do. They are binary, boolean, meaning they only understand 1 and 0, True or False, On and Off from a light switch brain.

Because of that Logic is such an **important concept** to be able to understand and manipulate computers properly.

For the logic studies we will keep to the basics, Propositional Logic.

![Pro](/images/logic/propositional-logic.jpg)

- Propositional Logic
    - Formalization
    - Evaluation
    - Properties

### But first, what is Logic?

> Logic is the science that studies principles and methods that distinguish good reasoning from bad one.

**Reasoning** is a mechanism that we use to obtain new information from existing information.

For this, logic studies the thoughts that have to do with reasoning.

* Are all thoughts linked to reasoning? 
    - **Indications** (Maximum Speed 60 Kms, Insert Card, etc.)
    - **Interrogations** (Will it take place today?, Is there food?, etc.)
    - **Exclamations** (hurry!!, come!!, etc.)
    - **Lament** (What a pity, what joy, etc.)
    - **Emotions** (I would like to live in a better world, I wish I could see John Lennon playing)
    
> *No, not all*

##### Thoughts that are linked to reasoning:
- Express information about something or someone
    - Today it is 15 degrees celsius.
    - John is taller than Peter.
    - The moon is made of cheese.
    - The order of the factors does not alter the product.
- These statements can only be TRUE or FALSE, they are binary!

##### Incorrect reasoning:
1. If the Canucks win the Stanley Cup everyone will go to the airport to receive them.
2. The Canucks are well received at the Airport.
3. Therefore the Canucks won the Stanley Cup.

##### Correct reasoning
1. If the Canucks win the Stanley Cup everyone will go to the airport to receive them.
2. The Canucks won the Stanley Cup.
3. Therefore the Canucks are well received at the Airport.

**1** and **2**: information that we have; *(premises)*

**3**: generated information *(conclusion)*

> Note that the order is important for the entire reasoning (argument) to be considered a **valid** and finally proven truth. And so is the order important in computers. They will blindly execute whatever we tell them to do, *even if it makes no sense at all!*

### Modeling 

In order to arrive to the previous conclusions, the reasoning
schemes are studied, the structure of the sentences and phrases
that intervene in the reasoning are analyzed and the validity or
invalidity of the same is verified.
The reasoning is modeled.

**What does it have to do with computing?**
 
> In IT, when we program, we are guided by logical principles, and we apply logic to do the right things in the right order.

### Elements of Propositional Logic

- Propositions (or statements)
- Atomic
- Molecular
- Link terms or connectives

#### Propositions (or statements)

- Sentences that describes a property about someone or something.
- It has precise words and a clear sense.
- Can be evaluated as **True** or **False**.

There are 2 types of propositions:

**Atomic:** 
- Simplest propositions that are indivisible.
    - John goes to the movies
    - It is raining today
    - It is sunny today
    - Tomorrow I'll be studying
    - I ate a pizza yesterday

**Molecular:** 
- Propositions composed of atomic propositions joined by link terms or connectives.

## Link terms (or connectives): 

> It links 2 propositions. 

Linked propositions can be atomic as well as molecular propositions.

### Conjunction **AND** (**^**): 
- Connects 2 propositions stating that the two occur simultaneously. 
- E.g.: John goes to the mall **and** Maria goes to the movies.

### Disjunction **'OR'** (**v**): 
- Connect 2 propositions stating that at least one of the two things happens or both at the same time.
- E.g.: John goes to the movies **or** Maria goes to the mall.

| How would be the variables and formula for this one?

### Negation **NOT** (**~**): 
- Denies what happens in the proposal to which it applies.
E.g.: Maria **does not** go to the mall. I **do not** live in Uruguay.

## Formalization

Every sentence has an underlying structure that shows how it
articulates the information elements.

The structure is "extracted" via a formalization process.

Understand the meaning of the sentence.
Identify Atomic Propositions 
Identify Connectives
Group into Molecular Propositions.

**Note:** The structure is also called a propositional form or statement form.

Check the example of the formalization process with the following
sentence:

![Atoms and Molecules](/images/logic/atom-molecule.png)

We can further increase the level of abstraction by introducing variables for each element. Atom 1, Atom 2 and Molecule 1. Their values could be something like:

`Atom 1 = p = "Roses are red"`

`Atom 1 = q = "Bananas are yellow"`

`Molecule 1 = p ^ q`

Formalization is a simple method to understand. But to correctly
apply it, requires practice and moments of understanding and
intuition.

A molecule can have other molecules and successively until it
reaches the atoms.

**As we see it:**
- At the most basic level I have **atoms**
- At the higher level I only have the **molecule** (composed of atoms).

# Bonus thinking

Let's convert a few statements into variables:
- Statement: "John goes to the mall and Maria goes to the movies" 
- Let **p** = "John goes to the mall"
- Let **q** = "Maria goes to the movies"

We end up with the molecule (formula):
- Conjunction: **p ^ q**

| How would be the variables and formula for Disjunction and Negation?

- Disjunction: 
- Negation:

**Convert the following statements into variables:**
- "Today is raining and the grass is wet"
- "I won't buy toilet paper and carry it with me"
- "Neither Jane or I drink"
- "The Cannucks did not win or the game is going longer"

> Practice: write a few more statements and try to fit them into variables.

### Interpretation

Let's suppose that we have two sentences that enunciate two different phenomena:
- If today rains, I won't take the bus
- If I don't get paid, I won't go to work

Note that both sentences have the same logical structure, 
 if **p** then **q**. Only **p** and **q** are "variables" having different values and an implication.

> if is read as implies and goes with the symbol **->**, so p -> q is read if p then q.


- If today rains, I won't take the bus.
- p -> q
- p = today rains
- q = I won't take the bus. 

**Let's practice:**

- If I don't get paid, I won't go to work.
- p -> q
- p = ?
- q = ?

**Questions:**
- What would be the value of **~p**?
- What would be the value of **~q**?

### Ambiguities

We can say the same thing in different ways:
- Today it is a sunny day.
- Today is sunny.
- It's a sunny day today.

> In formalization, this translates as a single atomic proposition.

**To formalize** consists of extracting the logical structure, we detach it from the meaning.

- Replacing sentences with symbols

**To interpret** is to give it meaning.

- Substitution of symbols by phrases

A sentence is formalized in a unique way.

The same structure can have multiple interpretations, so to understand that sometimes we need a truth table

### Truth tables

When interpreting an atomic propositions it can be True or False, and this is determined by contrasting the enunciated with the reality.

- "It's morning."
- "The window is open."

The molecular propositions (the formula) can be **True** or **False** too, but are determined from the truth or falsity of their atomic propositions first, and then evaluating the connectives.

Statement: "It's morning and the window is open." 

**How is it verified if a statement is true or false?**
> Using truth tables!

They basically tell us how the truths are calculated for the different molecular propositions.

- Consider a proposition **p** that can take one of two truth values: 
T (true) , or F (false).

| p     | ~p    |
|-------|-------|
| True  | False |
| False | True  |

**Note**: **~p** has the opposite value of **p**.

- Consider two propositions **p** and **q**. Each can take one of two truth values: either T (true), or F (false). 

 Hence, the truth values of p and q can be combined in four different ways now:

| p     | q     | Analysis     |
|-------|-------| -------------| 
| True  | True  | Both True  |
| True  | False | p is True and q is False  |
| False | True  | p is False and q is True  |
| False | False | Both False  |

That is cool, very cool, super cool, but how can we visualize conditions?

### Let's start with a Conjunction: (**^**)

| p     | q     | p ^ q   |
|-------|-------| --------| 
| True  | True  | True    |
| True  | False | False   |
| False | True  | False   |
| False | False | False   |

> Note that it is only true when both **p** and **q** is true.

### Let's do a Disjunction: (**v**)

| p     | q     | p v q   |
|-------|-------| --------| 
| True  | True  | True    |
| True  | False | True    |
| False | True  | True    |
| False | False | False   |

> Note that it true when either **p** or **q** is true.


### Again man, what does it have to do with computers?

When a computer is interpreting a confition, an if statement, a script, a command it will evaluate the expression and do the action or not, so whoever creates the software is the one responsible for making sure the logic will be followed. Hence the computer only follow instructions. This is what we call boolean logic, remember we said before that computers are boolean machines? There you go...

#### REMEMBER

- A sentence corresponds to a unique propositional form.
- Sentences always rest on a single structure. (Ambiguity removed)
- Boolean Logic


Every operation is reduced to:
 
- **AND** Conjunction (and)
- **OR** Disjunction (or)
- **NOT** Negation (not)
 
### Boolean Logic

![Boolean logic](/images/logic/boolean-logic.jpg)

**EXAMPLE:**
- s = "They are stealing"
- p = "It is day"
- q = "the windows is open"

A reasoning to know if they are stealing could be:
- "They are stealing if it's not day and the window is open"

Which converts to:
- s = NOT(p) AND q

or simply

- s = ~p ^ q

| p     | q     | ~p      | ~p ^ q |
|-------|-------| --------| -------|
| False | False | True    | False  |
| False | True  | True    | True   |
| True  | False | False   | False  |
| True  | True  | False   | False  |

### Connectives precedence

- Connector links two propositions only, except the NOT that applies to only one.
- This is just what precedes the connectors or link terms: Which have the highest priority for linking propositions.
- You can use "(...)" to make clear what articulates with what. We are good at recognizing links with parentheses.

**Major to minor precedence: (what is evaluated first)**

1. () parenthesis
2. ~ negation NOT
3. ^ conjuction AND
4. V disjunction OR

**So, like on base math:** You can represent an statement as:
- (p v ~q) ^ s

**Draw the truth tables for the statements:**

- ~p ^ ~q
- p v q v s
- p ^ (q v s)
- ~p v q ^ s
- (p ^ q) v ~s
