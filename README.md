# This project aims to employ Flownet 2 for object tracking

The code has been modified to adapt the project purpose. To run, one can leverage the prepare.ipynb (colab).

Unlike the original execution, we modify the model to run on the dataset which is suitable for **Direct** or **Sequential** integration by using optical flow.

To execute:
- Prepare dataset with proper image names, for e.g., swan/direct/[swan-001-002 contains swan-001.png and swan-002.png, swan-001-003,...]. This can be achieved by the function create_folders provided in the prepare.ipynb

- Enter the command: 
python main.py --inference --model FlowNet2 --save_flow \
--save ./datasets/bear/optical_flow/direct/ \
--inference_dataset ImagesFromFolder \
--inference_dataset_root ./datasets/bear/img/direct/ \
--resume checkpoints/FlowNet2_checkpoint.pth.tar
