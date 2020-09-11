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

We collected data from a total of six participants, where Participant 2 took part in multiple sessions to enable inter vs intra-user performance comparison.

| Participant | Session Date | Day # |
|:-----------:|:------------:|:-----:|
|    PID001   |  24/07/2019  |   1   |
|   PID002A   |  24/07/2019  |   1   |
|   PID002B   |  30/07/2019  |   7   |
|   PID002C   |  30/07/2019  |   7   |
|   PID002D   |  30/07/2019  |   7   |
|   PID002E   |  30/07/2019  |   7   |
|    PID003   |  31/07/2019  |   8   |
|    PID004   |  31/07/2019  |   8   |
|    PID005   |  01/08/2019  |   9   |
|    PID006   |  01/08/2019  |   9   |

We recorded data via naturalistic 'Activity Pathways', with human participants taking approx. 45 minutes per session of activities. This involved asking participants to behave in a natural way, as if they were at home, as they moved throughout the testbed (between the two rooms) to perform routine daily activities, such as: sleeping, dressing, brushing teeth, brushing hair, preparing coffee, preparing a sandwich, eating, reading a book/newspaper, and washing dishes.

The location labels in the dataset represent semantic zones (identified after footage review) where the participants spend the practically all of their time outside of transitional states between activities and locations. These zones are reflected in the image below:

![tag_map](/images/tag_map.png)

The RFID dataset contains a total of 25,924 snapshots of data, where snapshots were recorded at a rate of one snapshot per second. This therefore represents around 7 hours and 12 minutes of raw data.

In the CSV and ARFF files of the RFID data, there are 196 target features, which are the tag identifiers of the 196 floor tags used in the study. The identifiers of these tags are also provided in the ```tags.txt``` file, for reference. The placement of these tags is also identified in the above image.

The penultimate byte of the tag identifier represents the room in which the tag was placed:
* ```2222xxxx``` = kitchen
* ```3333xxxx``` = bedroom

## Citation

If you need to cite this dataset, please use the following citation:

R. Smith, Y. Ding, G. Goussetis, and M. Dragone
A COTS (UHF) RFID Floor for Device-Free Ambient Assisted Living Monitoring. In Proceedings of the 11th International Symposium on Ambient Intelligence (ISAmI), 2020.