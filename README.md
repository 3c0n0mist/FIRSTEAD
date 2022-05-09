# FIRST E.A.D (EEG Aided Detection)

### Borealis AI: LSI Program

#### Team: Anjali Chauhan, Anthony Wu, James Riddell, Sumit Meghlani

## First Aid Need Detection using EEG signals

### 1. Abstract

Working or Travelling in the backcountry carries inherent risk. In British Columbia (BC) there are 1900 incidents per year, out of which 2100 people have been rescued by 3000 volunteers in 79 SAR (Search and Rescue Groups) [Dwight Yochim]. The only mode of communication is a Satellite Emergency Messaging Device (SEND).these devices combine the functions of a GPS with a commercial satellite phone in text only (SMS) mode. They are not able to make voice calls, but they can send text messages through various gateways to email, mobile phones and to social media.
 
Triggering a SEND device means hitting the “SOS” or “911” button intended to issue an emergency alert call for help. When a SEND device is triggered, the following sequence of events occur:

- User’s position and request for help are sent through a commercial satellite system to a ground monitoring agency.
- Agency passes along the alert to the appropriate local responding agency. In British Columbia this is the Joint Rescue Coordination Centre (JRCC) in Victoria, BC.
- The JRCC determines what kind of response is required. For ground-based alerts they send the message to EMBC’s Emergency Coordination Centre in Saanichton, BC.
- The ECC activates the nearest BC ground search and rescue team.
- The team mobilises with resources depending on the location and severity of the incident.

In the 2021-22 winter season 35 people died in the US and the average annual deaths related to winter activity is 22.8 [BC Coroners Service] in BC. This number is likely to climb as it is getting harder to anticipate hazards given climate change and rising uncertainties related to snowpack. Assuming we have the data, we believe it would be beneficial if we can predict real time health conditions in case of an emergency based on a pattern extracted from the past. Having a prediction will allow SAR groups to mobilise resources accordingly.

### 2. Relevance

Mild traumatic brain injuries or concussions have become an increasing public health concern, affecting an estimated 42 million individuals annually. Approximately 15–20% of those who sustain concussions develop chronic symptoms and functional impairments that persist for months or years. 
In addition, stroke is the third highest cause of death worldwide after cancer and heart disease, and the number of stroke diseases due to ageing is set to at least triple by 2030. These are two of the most common medical emergencies reported to 911 responders followed by bleeding, seizures, and extreme pain from physical trauma. One issue with the current state of injury assessment is its reliance on self-report. By their nature, symptoms are subjective: There is no way to measure a headache other than to record what an individual reports. Deficits have been reported in a wide range of laboratory and neurophysiological outcome measures in asymptomatic individuals after concussion. This reliance on self-reported symptoms, therefore, means that diagnosis is less precise, intervention targets are more difficult to identify. Models that can predict real-time health conditions in case of a medical emergency are attracting increasing attention. We plan on designing and implementing a health monitoring system that can detect/predict the precursors of any severe medical condition in real time.

### 3. Proposed Approach

The problem of classifying emotions from EEG signals can be difficult, as parsing the various elements of the signal and further interpretation remains a challenging task due to the complex structure of the human brain. Additionally, elements of the input from an individual’s EEG scan lack obvious features which indicate specific emotions. Here we propose that application of deep neural architectures lend themselves well to handle the dimensionality of the input and may lead to extrapolation of learned abstractions which can indicate different neural activity. In their research, Lui et al. indicate promising results for emotion classification from EEG signals, achieving 89.49% and 92.86% test accuracies on different emotions on the DEAP dataset with their combination architecture which leverages CNNs in tandem with sparse auto-encoders [Liu et al., 2020]. Their model’s accuracy is proposed to have been attributed to the special context which CNNs provide in combination with nontrivial latent factors which the auto-encoder is able to extract. Here we suggest the power of machine learning to aid rescuers/marketing agents, as it facilitates production of quick predictions from signals which are otherwise too complex to interpret, making the difference in life or death decisions in which real-time actions are required. For this project we plan to apply the model from Lui et al.’s work, to the classification of emotions which indicate distress, and further plan to experiment with other NN mechanisms like attention to provide global context to the signals and hopefully achieve even greater classification accuracy.

### 4. References

1. [Dwight Yochim] BC Search & Rescue Association: Official Sar Association of BC

2. (Avalanche.org " accidents 2020)

3. [BC Coroners Service] Winter Activity Deaths, 2008/2009 – 2017/2018

4. [Liu et al., 2020] Liu, J., Wu, G., Luo, Y., Qiu, S., Yang, S., Li, W., and Bi, Y. (2020). Eeg-based emotion classification using a deep neural network and
sparse autoencoder. Frontiers in Systems Neuroscience, 14.


### 5. Resources

#### Videos
1. [Introduction to EEG](https://www.youtube.com/watch?fbclid=IwAR2JNrSRODGoz3uxln5Rlq5jai7g6lEXjYNqSpsdEryqPtOXjviWsBctqQ4&v=XMizSSOejg0&feature=youtu.be)

#### Readings
1. [EEG based emotion classification](https://www.frontiersin.org/articles/10.3389/fnsys.2020.00043/full)
2. [Recognition of consumer preferences using EEG](https://www.frontiersin.org/articles/10.3389/fnhum.2020.604639/full?fbclid=IwAR3EqkdBT7gsSLKSSrsvBzE71N8tpAFPLbu36EqSfDX_Nbr9nWq1YajRyuE)
3. [Analyzing Fear Using a Single-Sensor EEG Device](https://link.springer.com/chapter/10.1007/978-3-319-49616-0_8?fbclid=IwAR2bGLR9zEdBcK7PrsSA4ABnpkq5rZ80l9cE_nVnY1PRNQKuSVq_4lpwtjM)
4. [Emotion classification using EEG signals based on tunable-Q wavelet transform](https://www.researchgate.net/publication/329396567_Emotion_classification_using_EEG_signals_based_on_tunable-Q_wavelet_transform)
5. [Deep Learning-based EEG Analysis: A Systematic Review](https://iopscience.iop.org/article/10.1088/1741-2552/ab260c)
6. [A Wearable In-Ear EEG Device for Emotion Monitoring](https://www.mdpi.com/1424-8220/19/18/4014/htm)
7. [Machine learning from wristband sensor data for wearable, noninvasive seizure forecasting](https://onlinelibrary.wiley.com/doi/10.1111/epi.16719)
#### DATA
1. [Publicly available EEG data](https://sccn.ucsd.edu/~arno/fam2data/publicly_available_EEG_data.html)
2. [Open EEG Datasets provided by meagmohit](https://github.com/meagmohit/EEG-Datasets)
3. [SEED Dataset provided from BCMI Labs](https://bcmi.sjtu.edu.cn/home/seed/index.html)
4. [Pain EEG Data](https://osf.io/zys7t/)
#### Analysis
1. [EDA done on EEG](https://www.kaggle.com/code/ruslankl/eeg-data-analysis/notebook?fbclid=IwAR0grq6Wau_Pp5ZRiCMnyTgUoi2dh5V0sBOPC1ZQ9FYx6-vQ1Woi1bpLSRM)

#### Github
1. [NN for emotional classification](https://github.com/JJBalisan/Using-a-Neural-Network-to-Classify-EEG-Brain-Signals)
2. [EEG pain detection](https://github.com/BIAPT/eeg-pain-detection)

