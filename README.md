Executive Summary
This repository contains the end-to-end analysis and development of a Machine Learning model designed to mitigate product giveaway (overfilling) in large-scale food manufacturing lines. Through a data-driven approach, the root causes of variability in critical sub-processes (batter depositing, cream injection, and jam injection) were identified, and a predictive system based on Decision Trees was implemented.

The deployment of this model allowed for the dynamic calculation of the optimal injection pressure based on real-time fluid physical properties. This achieved a drastic reduction in raw material waste, delivering an annualized financial impact of approximately $30 million MXN.

Business Context
In high-volume manufacturing processes, the rheological variations of materials often force operators to over-dose the product to ensure compliance with legal weight requirements (Lower Control Limits - LCL). This project addresses the issue by transitioning the operation from a reactive process control (relying on operator judgment) to an AI-driven prescriptive control system.

Methodology and Key Variables
The project was divided into sequential phases, starting with an Exploratory Data Analysis (EDA) of the finished product, followed by a deep dive into the physics of each sub-process.

Through correlation analysis and statistical testing, it was determined that the deposited weight variation fundamentally depended on the following predictor variables:

Rework Percentage (%): Proportion of recirculated dough in the current batch.

Fluid Temperature (°C): Thermal impact on material behavior.

Fluid Viscosity (mPa.s): Resistance to flow under shear stress.

Injection Pressure (bar): The mechanical, system-controllable variable.

Model Architecture
To map the non-linear relationships between the fluid's thermodynamic properties and the injection mechanics, a Decision Tree model was trained. The algorithm takes the desired target weight alongside current temperature, viscosity, and rework percentage as inputs, and outputs the exact injection pressure required to minimize final weight variance.

Repository Structure
The code is organized into sequential computational notebooks documenting the entire project lifecycle:

01_diagnostico_FP.ipynb: Initial process capability evaluation (Cp, Cpk) and statistical diagnosis of finished product weight.

02_root_cause_depositing.ipynb: Root cause analysis for the base dough (Batter) behavior, modeling the interaction between temperature, viscosity, and rework percentage.

03_root_cause_cream.ipynb: Thermodynamic analysis and the impact of structural resistance loss during cream injection.

04_root_cause_jam.ipynb: Identification of the rheological tipping point in jam behavior under thermal stress.

06_optimized_process_simulation.ipynb: Interactive prescriptive control simulator. Deployment of the Machine Learning model to prescribe the optimal operating pressure.

07_model_evaluation_and_operational_accuracy.ipynb: Model performance evaluation (Accuracy, Mean Absolute Error) and final financial ROI quantification.

Results and Impact
Process Optimization: Significant reduction in process variability, allowing the production mean to be centered closer to the target weight without violating quality specifications.

Raw Material Savings: Drastic decrease in the consumption of batter, cream, and jam.

Financial Impact: Validated savings totaling approximately $30 million MXN annualized.

Technologies Used
Language: Python 3.x

Data Processing: Pandas, NumPy

Machine Learning: Scikit-Learn (Decision Trees)

Statistical Visualization: Seaborn, Matplotlib

Environment: Jupyter Notebooks

Author
Larry Eduardo Beresford Díaz Data & Continuous Improvement Specialist
