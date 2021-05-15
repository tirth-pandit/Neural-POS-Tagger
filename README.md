# Neural-POS-Tagger-NLP

Project Name: Create a Statistical or Neural POS Tagger<\br>
Details:
POS tagging is a very basic task in NLP and Computational Linguistics. However, as many
of you already know, the state of POS tagging for Indian Languages is quite a mess at the
moment. This project as two subparts.
In this project, teams are expected to use statistical classification or sequence labeling
techniques such as HMMs, CRFs or basic neural network models in order to create a POS
Tagger. Note that morphological features in agglutinative languages play an important role
in determining the POS of the word. Training data will be provided beforehand. You can
refer to the following papers for reference:


Team Details:
1. Tirth Pandit (2019201017)
2. Pratik Tiwari (2019201023)



Overview:

Baseline Model: <\br>
	HMM:<\br>

	CRF:

Neural Model:
	1. Dual Embedding + LSTM
	2. Dual Embedding + BILSTM

	Run Instruction:
		# Data File Path
		path = '/content/guj_art and culture_sample1.txt'
		name = 'art' # some name of file

		# model to run lstm/bilstm, opt = ADAM/RMSPROP/SGD
		mod = 'lstm'
		opt = 'ADAM'

		# Datapreperation
		train,test,word_to_idx,tag_to_idx,char_to_idx = data_loader(path)
		
		# Trained Model
		model= trainmodel(mod,opt,train,word_to_idx,tag_to_idx,char_to_idx)
		# model will be saved in pth location
		save(model,pth,mod,opt,name)
		
		# test model will return Y_True,Y_predict,predicted_tags
		y_true,y_pred,predicted_tags = testmodel(model,test,word_to_idx,tag_to_idx,char_to_idx)

	Model Checkpoints:
		LSTM: https://drive.google.com/file/d/1zjlh6U7Z5uA9FZPqHOrmfybrt9h5zpM-/view?usp=sharing 
		BILSTM: https://drive.google.com/file/d/1M4cKgkZlxa5weMNlP_yfrxqV75LQtJSr/view?usp=sharing
