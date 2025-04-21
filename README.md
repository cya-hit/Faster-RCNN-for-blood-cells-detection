# Faster-RCNN-for-blood-cells-detection
# Faster-RCNN用于血细胞检测  
## 环境：  
torch 1.9.0+cu111
pip install -r requirements.txt
将虚拟环境的当前目录切换到faster-rcnn\lib\，输入下行指令，进行编译：python setup.py build develop
将虚拟环境的当前目录切换到faster-rcnn\，输入下行指令，开始训练：python trainval_net.py --dataset pascal_voc --net res101 --epochs 50 --nw 1 --bs 1 --lr 0.0001 --cuda 
将虚拟环境的当前目录切换到faster-rcnn\，输入下行指令，开始测试：python test_net.py --dataset pascal_voc --net res101 --checksession 1 --checkepoch 50 --checkpoint 583 --cuda
将虚拟环境的当前目录切换到faster-rcnn\，输入下行指令，进行目标检测：python demo.py --net res101 --checksession 1 --checkepoch 50 --checkpoint 583 --cuda --load_dir models
![image](https://github.com/user-attachments/assets/b860519f-eab8-4f93-8475-e85593b45698)
