CNN for Spatial Feature Extraction: 
• The input video is broken into individual frames. A pre-trained or custom Convolutional 
Neural Network (CNN) is applied to each frame to extract spatial features (e.g., player 
positions, ball movement, etc.). CNNs are highly effective at detecting patterns such as 
edges, textures, and objects in images. 
• The extracted features from each frame represent high-level spatial information, which is 
then flattened or encoded into a feature vector. 
Frame Sequence Creation: 
• Instead of processing frames independently, the system organizes frames into sequences 
that correspond to a specific time window. This ensures that temporal relationships 
between frames (e.g., the buildup to a goal) are preserved. 
LSTM for Temporal Feature Extraction: 
• These feature vectors (representing frames) are fed sequentially into an LSTM network. 
LSTMs are designed to handle sequential data and can capture temporal dependencies by 
maintaining memory over time. This allows the system to recognize patterns in the flow 
of actions (e.g., a pass leading to a shot). 
• The LSTM processes the sequence and generates an output that captures the temporal 
dynamics, helping to identify when and how an action occurs. 
Action Classification: 
• The final step is to apply a classification layer (e.g., a softmax or fully connected layer) to 
the LSTM’s output to classify the action (e.g., goal, foul, etc.). The combination of CNN
extracted spatial features and LSTM-learned temporal features enables more accurate 
recognition of complex sports actions. 
Dataset used: 
• UCF50 is a widely-used action recognition dataset containing 50 action categories, many 
of which are sports-related, such as basketball, tennis, and soccer. It consists of real
world videos collected from YouTube, providing diverse scenarios and varying camera 
angles. For the Live Sports Action Detection project, UCF50 can serve as a valuable 
dataset for training and testing the CNN-LSTM model. It enables the model to learn from 
complex and varied sports actions, enhancing its ability to recognize and classify events 
in live sports broadcasts. The dataset's diversity makes it suitable for capturing the spatial 
and temporal dynamics of sports actions.
