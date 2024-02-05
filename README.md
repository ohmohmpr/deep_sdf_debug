# install environment

```sh
./install.sh
```

## Deep_SDF in DSP-SLAM default

```bash
python dsp_slam/reconstruct_frame.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 0
python dsp_slam/reconstruct_frame.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 50
python dsp_slam/reconstruct_frame.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 100
python dsp_slam/reconstruct_frame.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 500
python dsp_slam/reconstruct_frame.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 1000
```

## Deep_SDF in DSP-SLAM without render term

```bash
python dsp_slam/reconstruct_frame_no_render_term.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 0
python dsp_slam/reconstruct_frame_no_render_term.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 50
python dsp_slam/reconstruct_frame_no_render_term.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 100
python dsp_slam/reconstruct_frame_no_render_term.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 500
python dsp_slam/reconstruct_frame_no_render_term.py --config configs/config_kitti.json --sequence_dir data/dsp_slam/kitti/07 --frame_id 1000
```

## Jupyter notebook for cleaning data and extract to pcd extension

1. Evaluate optimization

```bash
python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/000/000003/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/000/000009/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/000/000011/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/000/000021/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/000/000030/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/000/000049/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/001/001000/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/001/001005/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/001/001006/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/001/001007/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/001/001027/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/001/001035/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/001/001038/pcd.npy

python ours/2_reconstruct_multiple_frame_argo_compare.py --config configs/config_kitti.json --sequence_dir data/P04/cleaned_data/001/001039/pcd.npy


# yaw
# code motion
# inconsidtent over time and no using for data of mulitple frame
# ablation first frame vs multiple frame
# methodology tracking optimization, kiss icp pv-rcnn deepsdf
# abstraction -> Briftly introduction 200 words
# 1. introduction: why? what? how? *Claims
# 2. Related works: mention the exising works
# 3. methodology: how we do that this
# 4. Experiemtn: explain result, desscribe dataset, evaluatuoin metric, baseline(yue pan paper), implementation deitail(parameter setting, learnng, ) show result. abltion, change some params -> should support claim
# 5. Conclusion: repeat abstraction and disadvatange , futre work how can we imrpove

```
Shashank:
1. The naming of pts_cam_pcd, T_cam_obj seems to be wrong. velodyne in place of cam seems correct to me.
2. The surface_points and pts_cam_pcd are not with a relative transform of T_cam_obj. small difference. Visible with car_no =  1; frame = 10
