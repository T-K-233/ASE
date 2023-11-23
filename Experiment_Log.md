
```bash
stiffness="50"
damping="10"
```

```
pip uninstall torch
conda install pytorch pytorch-cuda=12.1 -c pytorch -c nvidia
```

```python
torch.__version__
'2.1.0+cu121'
numpy.__version__
'1.21.1'
```

# Tasks

Screen #2:

our berkeley humanoid training

```bash
CUDA_VISIBLE_DEVICES=2 python ase/run.py --task HumanoidAMPGetup --cfg_env ase/data/cfg/bkl_humanoid_ase_sword_shield_getup.yaml --cfg_train ase/data/cfg/train/rlg/ase_humanoid.yaml --motion_file ase/data/motions/reallusion_sword_shield/dataset_reallusion_sword_shield.yaml --headless
```
Humanoid_23-09-57-04


Screen #3:

our berkeley humanoid training (curriculum)

```bash
CUDA_VISIBLE_DEVICES=3 python ase/run.py --task HumanoidAMPGetup --cfg_env ase/data/cfg/bkl_humanoid_ase_sword_shield_getup_curri.yaml --cfg_train ase/data/cfg/train/rlg/ase_humanoid.yaml --motion_file ase/data/motions/reallusion_sword_shield/dataset_reallusion_sword_shield.yaml --headless
```
Humanoid_23-10-02-28


#### Motion Data
```bash
python ase/run.py --test --task HumanoidViewMotion --num_envs 2 --cfg_env ase/data/cfg/humanoid_sword_shield.yaml --cfg_train ase/data/cfg/train/rlg/amp_humanoid.yaml --motion_file ase/data/motions/reallusion_sword_shield/RL_Avatar_Atk_2xCombo01_Motion.npy
```

