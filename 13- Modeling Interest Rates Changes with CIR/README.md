# Modeling Interest Rates Changes with CIR Model
This notebook is used to simulate changes in interest rates using the Cox-Ingersoll-Ross model, usually just called the CIR model. CIR model utilizes the mean reversion model which features parameters to control the speed of mean reversion as well as the long term average rate.
$$ dr_{t}=a(b-r_{t})\,dt+\sigma {\sqrt  {r_{t}}}\,dW_{t} $$

## Interactive simulation
The simulation utilizes **ipywidgets** for more interaction.
![enter image description here](.)