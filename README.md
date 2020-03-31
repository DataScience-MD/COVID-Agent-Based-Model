# COVID Infection Model

(C) 2020 Mark M. Bailey

## About
This repository contains an agent-based model simulating COVID transmission within social networks using Mesa.  Model parameters can be set in the 'model_params.py" file.  Produces a dataframe output over quasi-time (steps).

This is a work in progress and is intended for research purposes only.

## Model Description
This is an SIR (susceptible, infected, recovered) model for COVID.  Model parameters can be set to simulate the changes in these three variables, as well as the reproduction number (R0), over time.  A negative R0 would indicate that the epidemic is becoming extinguished.  This can be used to simulate the effects of social distancing.

## Model Parameters
* ptrans = Transmission probability.
* population = Total population within all containers.
* progression_period = Average number of days until disease outcome (death or recovery).
* interactions = Average number of interactions per person per day (decreases with social distancing).
* reinfection_rate = Probability of becoming reinfected after recovery.
* I0 = Initial probability of being infected.
* death_rate = Probability of dying after being infected for number of days in progession period.
* recovery_rate = Probability of recovering after being infected for number of days in progession period.
* steps = number of days to simulate the model.<br /><br />
* chaos (in model_functions.py 'build_network' function) = Adjusting this parameter allows for social distancing compliance uncertainty.

## Instructions for Use
* Update parameters in the 'model_params.py' file.<br />
* Execute the 'run.py' script.<br />
`python run.py -o <output_path>`