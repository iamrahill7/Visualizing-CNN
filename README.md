# Visualizing-CNN

**Purpose:** The code helps in understanding how the VGG16 model processes images at different layers, showing what the network "sees" and learns at each stage of its architecture.

1. **Model Loading and Visualization:**
   - Loads the pre-trained VGG16 model and shows its architecture.
   - Visualizes the model's structure using `plot_model`, providing a visual representation of the layers and their connections.

2. **Filter Extraction and Visualization:**
   - Iterates through the model's layers to find convolutional layers.
   - Extracts and prints the shape of the filters from each convolutional layer.
   - Retrieves the filters from the first convolutional layer, normalizes them for visualization, and displays 6 filters (each filter with its 3 RGB channels) using matplotlib. This shows what kinds of features the filters are designed to detect (e.g., edges, textures).

3. **Feature Map Extraction from an Input Image:**
   - Loads and preprocesses an input image (`sachin.jpg`) to the required format for VGG16.
   - Creates a new model that outputs the feature maps from the first convolutional layer.
   - Predicts and visualizes these feature maps, showing how the model's filters transform the input image into feature maps (patterns and features detected by the filters).

4. **Feature Maps from Multiple Layers:**
   - Creates another model to extract feature maps from multiple layers (layers 2, 5, 9, 13, and 17) of VGG16.
   - Predicts the feature maps for the input image for these selected layers.
   - Visualizes the feature maps of each selected layer to illustrate how the model learns increasingly complex features as you go deeper into the network (from basic edges and textures to more abstract patterns).

