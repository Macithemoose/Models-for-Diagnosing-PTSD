# Models-for-Diagnosing-PTSD
Logistic Regression and Transformer Models for Diagnosing PTSD from EEG data (94% accuracy on Transformer)

Data comes from [this dataset](https://osf.io/8bsvr/) by Su Mi Park.

As described in [this paper](https://www.frontiersin.org/journals/psychiatry/articles/10.3389/fpsyt.2021.707581/full), EEG data was collected from 945 patients. 850 of the patients were diagnosed with a mental disorder, and the other 95 patients were healthy controls. EEG data was collected by attaching 19-64 electrodes to patients, and recording of 5 minutes worth of EEG activity in resting state.

Patients were classified into 6 "general disorder" categories, including: Schizophrenia, mood disorders, anxiety disorders, Obsessive-Compulsive Disorder, addictive disorders, and trauma and stress-related disorders. They were also classified into 9 "specific disorder" categories: Schizophrenia, Depressive Disorder, Bipolar Disorder, Panic Disorder, Social Anxiety Disorder, Obsessive-Compulsive Disorder, Alcohol Use Disorder, Behavioral Addiction Disorder, Post-Traumatic Stress Disorder, Acute Stress Disorder, and Adjustment Disorder. 

<h2>
  Diagram:
</h2>

<div align="center">
  <img src="https://macithemoose.github.io/Models-for-Diagnosing-PTSD/Figures_and_Images/conceptMap.svg" alt="diagram" width=600 height=700>
</div>

<h2>
  Looking at the actual data:
</h2>

After collecting EEG data, the signals were transformed from the time domain into the frequency domain using the Fast Fourier Transform method. In the actual dataset, the columns that include "AB" signify the absolute power values from taking the Fast Fourier Transform.

Data that contains artifacts such as eye blinks, power line interference, or other potential noise-creating events were removed. The data was split into six major frequencies: delta (1-4 Hz), theta (4-8 Hz), alpha (8 - 12 Hz), beta (12 - 25 Hz), high beta (25 - 30 Hz), and gamma (30 - 40 Hz).

The coherence values between the 19 major electrodes, or synchronicity between each electrode, was also calculated as a way of maintaining spatial relationships between different regions of the brain. These were also included in the data.

The following is a representation of what the data looks like in a table:
![Image](https://macithemoose.github.io/Models-for-Diagnosing-PTSD/Figures_and_Images/eeg_data_table.png)


