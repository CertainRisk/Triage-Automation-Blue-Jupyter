# Blue Jupyter - Automating Triage with Jupyter Notebooks

## Introduction
In the realm of malware analysis, efficient and automated triage processes are crucial. Blue Jupyter offers a powerful solution by integrating Jupyter Notebooks for seamless and automated malware analysis. In this blog I will be learning  the process of setting up Blue Jupyter and utilizing Jupyter Notebooks for automation.

All content is from TCM Security's Course - Malware Analysis and Triage which I deeply recommend!

## Step 1: Clone the PMAT-lab Branch
Clone the PMAT-lab branch of the Blue Jupyter code repository by running the following command:

```bash
git clone --branch PMAT-lab https://github.com/HuskyHacks/blue-jupyter.git && cd blue-jupyter
```
## Step 2: Dockerized Installation

```bash
sudo docker build -t bluejupyter .
```

## Step 3: Launch Blue Jupyter
I created a docker container via Remnux.

```bash
sudo docker run -it -p 8888:8888 -v /home/remnux/blue-jupyter:/src bluejupyter`
```

## Step 4: Adding Malware Samples to Dropbox
I copied the samples from the PMAT-labs repository into the directory so I could access it in the container. 

A VirusTotal API key was needed to check over 20 samples' SHA256sum on VirusTotal and then output in the notebook both the Confidence level and Criticality level of the samples. 
- This automation is vital when you're dealing with many samples in order to determine the ones with the highest level of criticality.


# Automation - Malware Unicorn Jupyter Notebooks

Malware Unicorn Jupyter Notebooks provide a comprehensive platform for automating malware analysis triage. In this section, I will be learning the process of utilizing these notebooks to enhance your automation capabilities. 

I input this on Remnux in order to host the notebooks in the container. 
```bash
sudo docker run -it -p 8888:8888 -v /home/remnux/blue-jupyter:/src bluejupyter
```
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/4bde39c6-4c5f-4ea9-b692-747d856436f8)

- Imports and setup
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/ad3ee52e-8566-44a3-afc2-abd3aacf2407)

- Check Dropbox and Saved-Specimens folder
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/f69205c5-90b3-4b8a-b1fc-735c1ddb2b0c)

- Enumerating the Samples in Dropbox
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/e34fc5eb-1fdf-4fb6-b51a-cf422d26904a)

- Create a saved specimen directory for the specimens
- Defang the Samples!
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/37b38212-7512-4ad1-b999-3b4d016994e8)
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/9b0de46a-525a-423e-825f-23d1371e6418)

- SHA256sum File hashes
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/73855ef3-a019-4442-b279-c66899ae6384)

- StringSifter
Not only does StringSifter sift through all the strings in the sample and compile them in a nice log to look through, it provides a score next to each string it finds based on the level of severity it poses. 
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/b088e9bf-f805-4c74-8c08-aacd6d96cd28)
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/89a4cc48-ee13-462b-860f-7d226e6228f1)

- VirusTotal Analysis
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/72a32fb1-1d1b-460f-b9e3-282add123603)
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/ab14b589-6ad5-4a01-8d82-dfdc3e312254)
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/23307a32-ca28-4fad-83c6-116cb578d538)
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/ae4ba2ae-ced6-4a16-8458-b3ce41409e46)
![image](https://github.com/CertainRisk/Triage-Automation-Blue-Jupyter/assets/141761181/d09a0e26-a4b9-424f-9d04-4790549491b1)

Malware Unicorn Jupyter Notebooks empower analysts to automate malware analysis tasks effectively. Explore the provided notebooks and integrate them into your workflow for enhanced efficiency.
