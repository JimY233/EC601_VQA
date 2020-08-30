# EC601_VQA
Please read EC601_VQA_Jiaming Yu(U72316560).pdf first.  In this paper, we would review and explore VQA: Visual Question Answering. The first part of paper is the literature review of VQA, introducing VQA including its related work, common methods and dataset. This paper also reviews and reproduces others' approach on VQA. In this paper, we also explore the user cases of VQA like aided-navigation for blind individuals, image retrieval,automatic querying and so on. Besides, we analyze the current VQA and future work.

The code is the reproduce of others' work on VQA. The dataset is a simplified synthetic 2D images along with simple questions. The answer to the questions are limited to yes/no, colors and shapes. The model is a simplified joint embedding approach of CNN processing images and Bags of Words representations turning questions to vectors.

Run:

pip install -r requirement.txt      

//install the requirements

python gen_data/generate_data.py      

//you can change NUM_TRAIN and NUM_TEST in generate_data.py to change the number of training set and testing set. This step can be ignored because there are already 8000 training images and 2000 testing images. The data are generated in the file data/train/ and data/test/ respectively

python train.py      

//train the model for 10 epochs, derieve model.h5; you can change epochs in train.py to control the number of epochs; the process of training can be found in EC601_VQA_Jiaming Yu(U72316560).pdf

After 8 epochs training, the accuracy of the model reaches 76 percent on testing set. Then we generate another different 4k images training set and 1k testing set and train the model again for 10 epochs. The accuracy reaches 84 percent. Then we generate 8k images training set and 2k testing set and train the model for 10 epochs. The accuracy reaches 99 percent.

