## JEPA-for-RL
Hà Huy Hoàng - 21127610

<img width="685" height="382" alt="image" src="https://github.com/user-attachments/assets/e9c92008-c351-4701-b7a3-a319e3b41316" />

#JEPA
INPUT:
- Consecutive image frames: (f_{t-2}, f_{t-1}, f_t)
- Future frames for prediction: (f_{t-1}, f_t, f_{t+1})
- Action a_t (one-hot encoded)
OUTPUT:
-Latent Representation
The encoder maps image observations into a latent state representation used for RL.
#RL
INPUT:

- Output of the JEPA encoder
- Used as the state representation for RL

OUTPUT:

 Policy (Actor):

- Probability distribution over actions

Value Function (Critic)

- Expected return from state \(s_x\)

 Action

- Selected action to interact with the environment


