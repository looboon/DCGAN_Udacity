<h2>Submission 2</h2>

Some changes were
- Deeper Generator model
- Dropout in Discriminator
- Smaller value for leaky ReLU
- One sided label smoothing for d_loss 

Things to improve: 
- Use placeholder for keep_prob instead. See this [link](https://stackoverflow.com/questions/44971349/how-to-turn-off-dropout-for-testing-in-tensorflow) to know how.
- Implement Xavier Initialization.
