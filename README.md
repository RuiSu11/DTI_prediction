# DTI_prediction

Drug-target interaction (DTI) models are desgined for computationally predicting which proteins can be targeted by which drugs. Accurate DTI models are thought to facilitate drug discovery. Recently deep learning (DL) models show significant accuracy in predicting DTIs. Such deep learning (DL) models typically consist of two separate network structures that extract the features of drugs and target proteins separately. Then the extracted features are then concatenated, following which one or more fully connected layers are used to process the concatenated features and make binding predictions. 

Here I developed a deep learning DTI model, inspired by recent advanced techniques in DL including graph neural networks (GNNs) and the attention mechanism. To extract the drug features, a two layer GNN was used to extract the features of each atom, which are determined by its neighbour atom, second neighbour atom and itself. Indeed each each GNN layer is a graph attention network, in which the information flow between each pair of neighbouring nodes is through the widely used attention mechanism. For the target protein, I used a rather simple and common architecture, a three-layer convolutional neural network (CNN). 

Code please see att_GAT.ipynb

Description about this project will come later
