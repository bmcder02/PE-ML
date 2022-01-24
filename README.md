# PE-ML

    If you had 200,000 executables and you were tasked with finding which were malicious and which were benign, how would you go about it?

My attempt at PE machine learning using the Practical Security dataset. https://practicalsecurityanalytics.com/pe-malware-machine-learning-dataset/

For this challenge, I decided to add a couple of restrictions on how I can complete this model:
    
- Can't use any data from within the sample.csv (except the label of malicious/benign)
- Can't use any external apis (e.g. Virus Total)
- Must be static, no dynamic analysis
- Must be completely automated, I'm not manually diggen through 250k files. 

# The Features

I collected the following data for this ML project:
- File Size
- File Type: The 'type {file name}' result
- Entropy
- Strings
- PE Data
    - Imports 
    - Exports 
    - Size of Image
    - Size of Code
    - Size of Stack Reserve
    - Size of Stack Commit
    - Size of Heap Reserve
    - Size of Heap Commit
    - Number of Sections
    - Sections
        - Name
        - Size of Raw Data
        - Virtual Size
        - Characteristic: Code
        - Characteristic: Executable
        - Characteristic: Write

