# EC601_VQA
Please read EC601_VQA_Jiaming Yu(U72316560).pdf first. 

In this paper, we would review and explore VQA: Visual Question Answering. The first part of paper is the literature review of VQA, introducing VQA including its related work, common methods and dataset. This paper also reviews and reproduces others' approach on VQA. In this paper, we also explore the user cases of VQA like aided-navigation for blind individuals, image retrieval,automatic querying and so on. Besides, we analyze the current VQA and future work.

The code is the reproduce of others' work on VQA. The dataset is a simplified synthetic 2D images along with simple questions. The answer to the questions are limited to yes/no, colors and shapes. The model is a simplified joint embedding approach of CNN processing images and Bags of Words representations turning questions to vectors.

Run:

pip install -r requirement.txt      
//install the requirements

python gen_data/generate_data.py      
//you can change NUM_TRAIN and NUM_TEST in generate_data.py to change the number of training set and testing set. This step can be ignored because there are already 8000 training images and 2000 testing images. The data are generated in the file data/train/ and data/test/ respectively

python train.py      
//train the model for 10 epochs, derieve model.h5; you can change epochs in train.py to control the number of epochs; the process of training can be found in EC601_VQA_Jiaming Yu(U72316560).pdf

After 8 epochs training, the accuracy of the model reaches 76 percent on testing set. Then we generate another different 4k images training set and 1k testing set and train the model again for 10 epochs. The accuracy reaches 84 percent. Then we generate 8k images training set and 2k testing set and train the model for 10 epochs. The accuracy reaches 99 percent.


REFERENCES:

[1] M. Acharya, K. Kafle, and C. Kanan. Tallyqa: Answering complex
counting questions. In Proceedings of the AAAI Conference on Artificial
Intelligence, volume 33, pages 8076–8084, 2019.

[2] P. Anderson, X. He, C. Buehler, D. Teney, M. Johnson, S. Gould, and
L. Zhang. Bottom-up and top-down attention for image captioning
and visual question answering. In Proceedings of the IEEE conference
on computer vision and pattern recognition, pages 6077–6086, 2018.

[3] J. Andreas, M. Rohrbach, T. Darrell, and D. Klein. Deep compositional
question answering with neural module networks. corr abs/1511.02799
(2015). arXiv preprint arXiv:1511.02799, 2015.

[4] S. Antol, A. Agrawal, J. Lu, M. Mitchell, D. Batra, C. L. Zitnick, and
D. Parikh. Vqa: Visual question answering. In Proceedings of the
IEEE International Conference on Computer Vision (ICCV), December
2015.

[5] A. Das, S. Kottur, K. Gupta, A. Singh, D. Yadav, J. M. Moura, D. Parikh,
and D. Batra. Visual dialog. In Proceedings of the IEEE Conference
on Computer Vision and Pattern Recognition, pages 326–335, 2017.

[6] Y. Goyal, T. Khot, D. Summers-Stay, D. Batra, and D. Parikh. Making
the v in vqa matter: Elevating the role of image understanding in
visual question answering. In Proceedings of the IEEE Conference on
Computer Vision and Pattern Recognition, pages 6904–6913, 2017.

[7] J. Johnson, B. Hariharan, L. van der Maaten, L. Fei-Fei,
C. Lawrence Zitnick, and R. Girshick. Clevr: A diagnostic dataset
for compositional language and elementary visual reasoning. In
Proceedings of the IEEE Conference on Computer Vision and Pattern
Recognition, pages 2901–2910, 2017.

[8] K. Kafle and C. Kanan. Visual question answering: Datasets, algorithms,
and future challenges. Computer Vision and Image Understanding,
163:3–20, 2017.

[9] R. Shrestha, K. Kafle, and C. Kanan. Answer them all! toward
universal visual question answering models. In Proceedings of the
IEEE conference on computer vision and pattern recognition, pages
10472–10481, 2019.

[10] Y. Srivastava, V. Murali, S. R. Dubey, and S. Mukherjee. Visual
question answering using deep learning: A survey and performance
analysis. arXiv preprint arXiv:1909.01860, 2019.

[11] P. Wang, Q. Wu, C. Shen, A. Dick, and A. van den Hengel. Fvqa:
Fact-based visual question answering. IEEE transactions on pattern
analysis and machine intelligence, 40(10):2413–2427, 2018.6

[12] Q. Wu, D. Teney, P. Wang, C. Shen, A. Dick, and A. van den Hengel.
Visual question answering: A survey of methods and datasets. Computer
Vision and Image Understanding, 163:21–40, 2017.

[13] K. Xu, J. Ba, R. Kiros, K. Cho, A. Courville, R. Salakhudinov, R. Zemel,
and Y. Bengio. Show, attend and tell: Neural image caption generation
with visual attention. In International conference on machine learning,
pages 2048–2057, 2015.

[14] Y. Zhang, J. Hare, and A. Prugel-Bennett. Learning to count objects ¨
in natural images for visual question answering. arXiv preprint
arXiv:1802.05766, 2018.
