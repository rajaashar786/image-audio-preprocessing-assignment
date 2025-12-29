# image-audio-preprocessing-assignment
## Question 1: Image Preprocessing (CIFAR-10)

- **Dataset**: CIFAR-10 (test split, automatically downloaded via torchvision)
- **Selected Samples**: Two images from the test set (e.g., deer and automobile)
- **Preprocessing Steps Demonstrated**:
  - Resize to 64×64
  - Grayscale conversion (shown with replicated channels for visualization)
  - Random horizontal flip (applied with probability 1.0 for demo)
  - Random rotation (±30°)
  - Color inversion
- **Visualization**: Side-by-side display of the original images and each transformation applied individually
- **Final Pipeline**:
  - Resize to 64×64
  - Convert to tensor (values in [0.0, 1.0])
  - Normalize using CIFAR-10 mean and std:
    - mean = [0.4914, 0.4822, 0.4465]
    - std  = [0.2023, 0.1994, 0.2010]
- **Output**: A batch tensor containing the two preprocessed images
- **Final Tensor Shape**: [2, 3, 64, 64] (batch_size=2, channels=3 (RGB), height=64, width=64)
- **Additional Info Printed**:
  - Final tensor shape
  - Min/max pixel values after normalization

**Running the script** will automatically download the CIFAR-10 dataset (if not already present), display the visualization of all transformation steps, and print the final tensor details.