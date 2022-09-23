# DTI_prediction

Drug-target interaction (DTI) models are desgined for computationally predicting which proteins can be targeted by which drugs. Accurate DTI models are thought to facilitate drug discovery. Recently deep learning (DL) models show significant accuracy in predicting DTIs. Such deep learning (DL) models typically consist of two separate network structures that extract the features of drugs and target proteins separately. Then the extracted features are then concatenated, following which one or more fully connected layers are used to process the concatenated features and make binding predictions. 

Here I developed a deep learning DTI model, inspired by recent advanced techniques in DL including graph neural networks (GNNs) and the attention mechanism. The drug inputs are the actually chemical structures of the molecule. To extract the drug features, a two layer GNN was used to extract the features of each atom, which are determined by its neighbour atom, second neighbour atom and itself. Indeed each each GNN layer is a graph attention network, in which the information flow between each pair of neighbouring nodes is through the widely used attention mechanism. For the target protein, the inputs are the amino acid sequence. I used a rather simple and common architecture, a three-layer convolutional neural network (CNN), which extracts the features for each amino acid. 

The extracted features of the drug and the target are often simply concatenated for furthur prediction. This simple treatment may not produce interpretable predictions, considering the complicated physical interactions between the drug and the target. A much more reasonalbe is to use the attention mechanism, such that the associations between each amino acid in the target and each atom in the drug are quantified. Thus, I used the attention mechanism to concatenate the drug and target features, following which a fully connected layers are used to make the prediction (dissociation constant, Kd). 

Code please see att_GAT.ipynb

Description about this project will come later
