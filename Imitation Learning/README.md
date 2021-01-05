This is a quick summary of the project:
- For the Deep RL module at Berkeley
- The homework topic was imitation learning with a second task using data aggregation
- This project used PLE and pygame to make the environment catcher

Files:
- Behavioural Cloning.ipynb -> code for basic imitation learning 
- Data Aggregation.ipynb -> code for basic imitation learning + dagger implementation
- Objects.ipynb -> game objects
- Utils.ipynb -> useful functions
- Game.ipynb -> game environment
- Expert Data -> the data collected to train both iterations of the model. Perfect data used bot as policy expert 
- model_imitation_1hr.h5 -> model after training behavioural cloning for ~ 1hr
- model_imitation_dag.h5 -> model with dag implementation after 3 iterations
- model_imitation_dag_1.h5 -> previous model had bias to right, this corrected that


A few notes:
- Differences in human and robotic policy maker led to problems in getting the highest scores, would want to keep to one or the other
- Keeping samples constant between classes only worked if left and right had the same weighting, otherwise would be constantly pulled to one side
