



![Alt text](imgs/alz1.png | width=100)





# Usage

- Environment

    - Python 3.6

    - TensorFlow 2.2, TensorFlow Addons 0.10.0

    - OpenCV, scikit-image, tqdm, oyaml

    - *we recommend [Anaconda](https://www.anaconda.com/distribution/#download-section) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html#linux-installers), then you can create the TensorFlow 2.2 environment with commands below*

        ```console
        conda create -n tensorflow-2.2 python=3.6

        source activate tensorflow-2.2

        conda install scikit-image tqdm tensorflow-gpu=2.2

        conda install -c conda-forge oyaml

        pip install tensorflow-addons==0.10.0
        ```

    - *NOTICE: if you create a new conda environment, remember to activate it before any other command*

        ```console
        source activate tensorflow-2.2
        ```

- Dataset

    - Alzheimer’s Disease Neuroimaging Initiative (ADNI) dataset can be downloaed  [here](http://adni.loni.usc.edu/)

    

- Example of training

    ```console
    CUDA_VISIBLE_DEVICES=0 python train.py --dataset adni
    ```

    - tensorboard for loss visualization

        ```console
        tensorboard --logdir ./output/summer2winter_yosemite/summaries --port 6006
        ```

- Example of testing

    ```console
    CUDA_VISIBLE_DEVICES=0 python test.py --experiment_dir ./output/adni
    
    
    ```
    
- ADNI Results
    
    ![Alt text](imgs/abtoan.png)
