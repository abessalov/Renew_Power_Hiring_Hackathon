# Renew Power Hiring Hackathon
This hackathon have been hosted on MachineHack platform: https://machinehack.com/hackathons/renew_power_hiring_hackathon/overview.

---

## Files description

- Machinehack_code.ipynb - main script for generating the final submission. 
- Machinehack_presentation.pdf - presentation with the quesions from organizators.
- Machinehack_code.ipynb - script with graphs for presentation.
- startup.py - initial script that run in every notebook when started (from \.ipython\profile_default\startup)
- develop - the directory with exploratory scripts for training different models:
    - lightgbm, xgboost, random forest, knn, mlp;
    - parameters searching; 
    - feature selection

## Data description
In this hackathon, ReNew Power shared minute-wise normalized data of wind speed, power and temperature data for multiple components of a wind turbine. The company is looking to create a model to get an ideally functioning turbine’s expected rotor bearing temperature. It will then use the model to check the deviation of the actual rotor bearing temperature of the faulty turbine from the expected temperature. 

We have the following features as input divided into train and test sets (909604 and 303202 rows respectively):

![Screenshot](img/data.png)

## Results
The evaluation metric of that competition is Mean Average Percentage Error. The best MAPE on the public leader-board is 0.00943

After some explorations we decided to train individual models for every unique turbine_id because they are different. In the table below placed MAPE scores of the best found models on the validation set:

![Screenshot](img/results.png)

