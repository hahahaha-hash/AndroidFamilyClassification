This is the repository for our malware family classification system, which is introduced on our paper: 

Sercan Türker, Ahmet Burak Can, AndMFC: Android Malware Family Classification Framework, IEEE 30th Annual International Symposium on Personal, Indoor and Mobile Radio Communications (PIMRC) Workshops - W4: Workshop on Machine Learning for Security and Cryptography: ML4SeC, 2019.

In this repository, there are some scripts and programs that parses Android applications and extracts features to train machine learning classifiers which classifies malwares into their families.

The android malware applications are parsed with "apkParser" script. This is a bash script and is written in Ubuntu platform. The script parses all apk files in a directory with Apktool and generates an output folder for each apk file.

The other bash script called "apiCallExtractor" extracts api calls of each application. The script uses smali folders for this operation.

The features are filtered with FeatureSelection.py script according to the importance during classification.

FeatureExtractor.cs program uses new feature set and extracts feature values for each application. It produces a text file that contains 0 and 1 values that corresponds the existing of feature.

In Classifiers folder, the scripts of the machine learning classifiers can be found.
