# Covid-Diagnostics
Using machine learning to monitor for Covid-19 infections

In the spring of 2020, individual cities, counties, and states began implementing restrictive mitigation strategies around the novel corona virus SARS-C0V-2. Many feared either contracting or spreading of the virus and took to quarantining at home for weeks or months at a time. Many institutions scrambled to find ways to resume semi- normal activity while at the same time keeping all involved safe and comfortable. Different testing solutions were rolled out as a mechanism for helping individuals know if they were infected with the virus so that they could make better informed decisions. But many of these tests are slow, expensive, inconvenient, and too inaccurate for individuals to take on a regular basis. What is needed is an easier way to test and monitor for Covid-19 that empowers more people to make responsible health decisions. The goal is is to build a classification machine learning model that can accurately diagnose Covid-19 using bio-metrics gathered either by api’s to Apple’s Health app or from user input to specific questions such as “Are you currently experiencing a cough?”. Inputs would include numeric values (body temperature, pulse, and Sp02) to output a class output of either 1 or 0, with 1 representing a Covid-19 diagnosis and 0 representing no indication of infection with Covid-19. A further model would be developed which takes binary classification values such as the existence of a cough, sore throat, and headache and again outputs a class value of 1 or 0, with 1 representing a Covid-19 diagnosis and 0 representing no indication of infection with Covid-19. Each feature in the second model will be represented as a 1 if the user is experiencing the symptom or a 0 if they are not. 

This project makes attempts to build models that can predict Covid-19 using symptoms gathered both from an Apple Watch Series 6 and from questions posed to users about symptoms they may be experiencing. One of the logistic regression models build from just Sp02 and Pulse data was then used in an iOS app project seen here: https://github.com/crweaver225/Covid-Monitor. 

This project has two Jupyter Notebooks that handle the two different datasets. The first one is Vitals_Diagnostics.ipynb which handles the vitals dataset containing Sp02, Pulse, and Temperature data along with a postive or negative Covid result. The second notebook is Symptom_Diagnostics.ipynb which has many different binary features representing different possible symptoms the user is experiencing and four possible targets (Flu, Covid-19, allergies, common cold). 

### Requirements
You will need the following libraries and languages in order to run this project:
1. Python 3.5 or higher
2. Scikit-Learn
3. numpy 
4. Matplotlib 

All of these can be installed use the pip package manager or Anaconda. 

### Summary Results
The logistic model ended up having an 80% precision and 94% specificity.
<p align="center">
  <img src="/screen-shots/1.png" width="350"/>
</p>

With more detailed information on symptoms provided by the user, we can build a random forest model that can differentiate between Covid-19, allergies, the flu, and a cold with high precision and specificity. 
<p align="center">
  <img src="/screen-shots/3.png" width="350"/>
</p>
