# Credit DavidSandberg (repo owner) and RuiJue (pretrained models)

- Original Repo (By David Sanberg): https://github.com/davidsandberg/facenet
- Models (Trained by RuiJue, Shared by Adriel): https://drive.google.com/drive/folders/1Z0wTa879sdUYWdxT45RmINbYxA_yoxZ-?usp=sharing


## Instructions:
1. conda create -n facenet_rj python=3.7 -y
2. conda activate facenet_rj
3. pip install -r HM_requirements
4. Run "export PYTHONPATH=$PYTHONPATH:<local path for facenet-master/src>"
5. Download pretrained models from the gdrive
6. cd contributed/
7. Run "python export_embeddings.py --model_dir <path for rj_models/20170512-110547> --data_dir ../data/images --is_aligned False"
  - --is_aligned depends on whether your images are aligned and face-extracted.
8. Output:
  - /contributed folder: label_strings.npy, labels.npy, embeddings.npy (128-dim because facenet). 
  - /data/images_faces_detected: faces detected for each image

### I/O
- INPUT: data/images/* 
- OUTPUT: data/images_faces_detected/* and /contributed
