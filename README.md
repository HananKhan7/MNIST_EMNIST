## EMNIST Letters
- For letters we require to change the output layer, which will be part of fine-tuning during TL.
## Further suggestions

- **Create a dataset of EMNIST consisting of both letters and digits with 37 labels (10 digits and 27 letters) and use that for further evaluation and transfer learning, look into EMNIST bymerge and EMNIST balanced**

- The ByMerge EMNSIT data has 47 classes with 11 random lowercase letters at the end, either remove those to avoid complication or choose ByClass variant of EMNIST, which has 62 classes (seperate for upper and lowercase).
  - Better to just remove additional lowercase letters to avoid complicating things. (Mention that custom dataset was used) **(DONE)**

- TL from MNIST to EMNIST
  - Train the MNIST model **(DONE)**
  - save the model **(DONE)**
  - import as base model and change input/output layers (Only output layer) **(DONE)**
  - Evaluate model performance without training **(DONE)**
  - Extract a random batch of EMNIST 36 **(DONE)**
  - Fine-tune the model on EMNSIT 36 **(DONE)**
  - Evaluate again **(DONE)**
  - compare the results with a model train from scratch on EMNIST 36. **(DONE)**
- Further steps
  - Use Tensorflow architecture and test it out for TL.
  - Make a mathematical representation of TL steps.
    - look into professor's suggestion from the photo.
    - Keep it simple in representation take a few classes from MNIST and a few classes from EMNIST.
    - Main idea is to showcase the difference in the mathematical equations before and after adding new neurons for TL (not iteration by iteration). 
    - ~ show how the old weights can be frozen and only new weights are updated (Highly unlikely, trained transferred weights serve as good starting points)
  - **USE THE SAME SUBSET OF EMNIST FOR BOTH TL AND EMNIST MODEL (FROM SCRATCH), currently the subsamples are randomly selected seperately for both.**
  
  - Make a presentation

- For later

  - Look into additional evaluation steps that can be utilized.

  - (For later)reduce the training data for MNIST and then impement TL by fine-tuning with additional training data from EMNIST letters and see if their is any difference on performance on MNIST

### In progress steps