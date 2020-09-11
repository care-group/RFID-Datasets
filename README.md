# RFID Datasets

This repository contains the RFID dataset detailed in our paper 'A COTS (UHF) RFID Floor for Device-Free Ambient Assisted Living Monitoring'. Also provided is the associated smart home data (exported from OpenHAB), that we did not discuss in the paper, but may be of interest as supplementary data or as training data for an activity/localisation classification in its own right.

Files from both sources are provided in CSV and ARFF format. The data is presented linearly over time, from Participant 1 - Participant 6. Activity, location, participant ID, and Unix timestamp are provided for each entry.

## Testbed Information

We conducted the experiments in the [Robotic Assisted Living Testbed](https://ralt.hw.ac.uk/) at Heriot-Watt University.

The RALT is a 60 sq. metre fully furnished apartment, complete with combined living/dining/kitchen area, bedroom, and bathroom.

## Hardware Information

For the collection of the RFID data, we utilised a hardware setup of:
* 1 x IMPINJ Speedway Revolution R420 UHF RFID Reader
* 4 x Laird Far-Field RAIN RFID Antenna (865-868MHz)
* Approx. 196 x IMPINJ RFID Monza 4QT Tags (on floor)

We placed four tags each on 60 sq. cm Ethylene Vinyl Acetate (EVA) floor mats, for easy installation.

We placed these mats across the the bedroom and kitchen of the testbed.

![bedroom_with_tags](/images/bedroom_with_tags.JPG)

The reader was configured to operate in 'AutoSet Dense Reader Deep Scan' mode, for wide coverage.

## Dataset Information

We recorded data via naturalistic 'Activity Pathways', with human participants taking approx. 45 minutes per session of activities.

The RFID dataset contains a total of 25,924 snapshots of data.

## Citation

If you need to cite this dataset, please use the following citation:

R. Smith, Y. Ding, G. Goussetis, and M. Dragone
A COTS (UHF) RFID Floor for Device-Free Ambient Assisted Living Monitoring. In Proceedings of the 11th International Symposium on Ambient Intelligence (ISAmI), 2020.