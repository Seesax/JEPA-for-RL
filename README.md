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
$s_x = f_\theta(x)$
-Target Embedding
\[
s_y = f_{\theta'}(y)
\]
-Predicted Future Embedding
\[
s_{py} = g_\phi(s_x, a_t)
\]
The encoder maps image observations into a latent state representation used for RL.
#RL
INPUT:
Latent State
\[
s_x
\] 
- Output of the JEPA encoder
- Used as the state representation for RL
OUTPUT:
 Policy (Actor)
\[
\pi(a | s_x)
\]

- Probability distribution over actions
Value Function (Critic)
\[
V(s_x)
\]

- Expected return from state \(s_x\)
 Action
\[
a_t
\]

- Selected action to interact with the environment


