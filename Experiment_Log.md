Created a `amp_humanoid_better.xml` file with all joints set to 

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


#### Pre-Training
```bash
python ase/run.py --task HumanoidAMPGetup --cfg_env ase/data/cfg/humanoid_ase_sword_shield_getup.yaml --cfg_train ase/data/cfg/train/rlg/ase_humanoid.yaml --motion_file ase/data/motions/reallusion_sword_shield/dataset_reallusion_sword_shield.yaml --headless
```


#### Motion Data
```bash
python ase/run.py --test --task HumanoidViewMotion --num_envs 2 --cfg_env ase/data/cfg/humanoid_sword_shield.yaml --cfg_train ase/data/cfg/train/rlg/amp_humanoid.yaml --motion_file ase/data/motions/reallusion_sword_shield/RL_Avatar_Atk_2xCombo01_Motion.npy
```

