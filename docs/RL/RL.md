# Reinforcement Learning
## Basic concepts
 - state: describes the agent's status with respect to the environment
 - action: 
 - policy: tells the agent which actions to take at every state
 - reward: a real number we get after taking an action.(can be interpreted as a human-machine interface)
   - the reward depends on the state and action, but not the next state
 - trajectory: a state-action-reward chain
 - return: the return of this trajectory is the sum of all the rewards collected along the trajectory
 - discounted return: 
 - episode: 
### Markov decision process(MDP)
Key elements of MDP:
- Sets:
  - State: the set of $\mathcal{S}$
  - Action: the set of actions $\mathcal{A}(s)$is associated for stater s  $s\in\mathcal{S}$
  - Reward: the set of rewards $\mathcal{R}(s,a)$
- Probability distribution:
  - State transition probability: at state $\mathcal{s}$, taking action $a$, the probability to transit to state $\mathcal{s'}$ is $p(s'|s,a)$
  - Reward probability: at state $\mathcal{s}$, taking action $a$, the probability to get reward $r$ is $p(s,a)$
- Policy: at state $\mathcal{s}$, the probability to choose action $a$ is $\pi(a|s)$
- Markov property: memoryless property

$$
\begin{align*}
p(s_{t+1} \mid a_{t+1}, s_t, \ldots, a_1, s_0) &= p(s_{t+1} \mid a_{t+1}, s_t) \\
p(r_{t+1} \mid a_{t+1}, s_t, \ldots, a_1, s_0) &= p(r_{t+1} \mid a_{t+1}, s_t)
\end{align*}
$$ 
## State Value and Bellman equation
### State Value
Consider the following single-step process:
$$
S_t\xrightarrow{A_t}R_{t+1},S_{t+1}
$$
- $t,t+1$: discrete time instances
- $S_t$: state at time $t$
- $A_t$: the action taken at state $S_t$
- $R_{t+1}$: the reward obtained after taking $A_t$
- $S_{t+1}$: the state transited to after taking $A_t$
Note that $S_t$,$A_t$,$R_{t+1}$are all random variables.
This step is governed by the following probability distributions:
- $S_t\rightarrow A_t$ is governed by $\pi(A_t=a\mid S_t=s)$
- $S_t,A_t\rightarrow R_{t+1}$ is governed by $p(R_{t+1}=r\mid S_t=s,A_t = a)$
- $S_t,A_t\rightarrow S_{t+1}$ is governed by $p(S_{t+1}=s'\mid S_t=s,A_t=a)$
At this moment, we assume we know the model(i.e., the probability distributions)!

Consider the following multi-step trajectory:

\[
S_t \xrightarrow{A_t} R_{t+1}, S_{t+1} \xrightarrow{A_{t+1}} R_{t+2}, S_{t+2} \xrightarrow{A_{t+2}} R_{t+3}, \dots
\]

The discounted return is
\[
G_t = R_{t+1} + \gamma R_{t+2} + \gamma^2 R_{t+3} + \dots
\]

- $\gamma \in (0, 1)$ is a discount rate.
- $G_t$ is also a random variable since $R_{t+1}, R_{t+2}, \dots$ are random variables.

The expectation (or called expected value or mean) of $G_t$ is defined as the *state-value function* or simply *state value*:

\[
v_{\pi}(s) = \mathbb{E}[G_t \mid S_t = s]
\]

Remarks:
- It is a function of $s$. It is a conditional expectation with the condition that the state starts from $s$.
- It is based on the policy $\pi$. For a different policy, the state value may be different.


**Q:** What is the relationship between return and state value?

**A:** The state value is the mean of all possible returns that can be obtained starting from a state. If everything -- $\pi(a \mid s)$, $p(r \mid s, a)$, $p(s' \mid s, a)$ -- is deterministic, then state value is the same as return.


