### Imbalanced Data Set

- **Class Labels** should be `Balanced` otherwise it Predicts a **Biased Output** or Classify Biased to only one Class Label.

### Stratified Sampling
- Create a Sample containing `Equal` number of Each `Class Labels` to Train the Model

### Up Sample Minority Class
- Randomly Duplicate the Observations in order to reinforce the Learning of Data
- Sampling with `Replacement`
- First Seperate Observations for Each Class.
- Resample Minority Class with Replacement, Setting Number of Samples to Match with Majority Class.
- Combine the Up Sampled Data with Orignal Majority Class Dataframe.

### Down Sample Majority Class
- Randomly Removing Observations from Majority Class ( Resampling **without** Replacement )
- First Seperate Observations for Each Class.
- Resample Majority Class `without` Replacement, Setting Number of Samples to Match with Minority Class.
- Combine the Down Sampled Data with Orignal Minority Class Dataframe.

### Change Evaluation for Better Performance
- Use **Stratified K Fold Cross Validation** with Equal Class Labels to Train the Model

### Decision Tree
- Decision Tree performs well on `Imbalanced Dataset` because there **Hierarchical Structure**  allows to Learn from both Classes.
