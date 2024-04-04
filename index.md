



# 16-825 Assignment 4

# 1. 3D Gaussian Splatting

## 1.1 3D Gaussian Rasterization

|   ![](images/Q1/output/q1_render.gif)   |
| :-------------------------------------: |
| **Rendering the 3D Gaussian splatting** |



## 1.2 Training 3D Gaussian Representations

|                         Output GIFs                          |
| :----------------------------------------------------------: |
|        ![](images/Q1/output/q1_training_progress.gif)        |
| <img src="images/Q1/output/q1_training_final_renders.gif" style="zoom: 200%;" /> |

Hyperparameters used: 

- Learning Rate:
  - `pre_act_opacities`:  0.05
  - `pre_act_scales`: 0.001
  - `colours`: 0.001
  - `means`: 0.0001
- No of Iterations: 1000
- `PSNR`: 27.536
- `SSIM`: 0.914

## 1.3 Extensions

### 1.3.1 Rendering Using Spherical Harmonics 

|            DC Harmonics             |          Spherical Harmonics          |
| :---------------------------------: | :-----------------------------------: |
| ![](images/Q1/output/q1_render.gif) | ![](images/Q1/output/q1_render_1.gif) |

Comparison of DC and spherical harmonics. As we can see below renderings from spherical harmonics has the colours and features are more sharp and intricate. 

|         DC Harmonics Images         |      Spherical Harmonics Images       |
| :---------------------------------: | :-----------------------------------: |
| ![](images/Q1/output/q1_render.gif) | ![](images/Q1/output/q1_render_1.gif) |
|                                     |                                       |



# 2. Diffusion-guided Optimization

## 2.1 SDS Loss + Image Optimization 

|               Prompt               |                       Without Guidance                       |                        With Guidance                         |
| :--------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|            A Hamburger             |    ![](images/Q2/image/a_hamburger/output_a_iter_400.png)    | ![](images/Q2/image/a_hamburger_guided/output_a_iter_1900.png) |
|                                    |                  Trained for 400 Iterations                  |                 Trained for 2000 Iterations                  |
|          A standing corgi          | ![](images/Q2/image/a_standing_corgi_dog/output_a_iter_600.png) | ![](images/Q2/image/a_standing_corgi_dog_guided/output_a_iter_1999.png) |
|                                    |                  Trained for 600 Iterations                  |                 Trained for 2000 Iterations                  |
| A painting of a sunset over a lake | ![](images/Q2/image/a_painting_of_a_sunset_over_a_lake/output_a_iter_1300.png) | ![](images/Q2/image/a_painting_of_a_sunset_over_a_lake_guided/output_a_iter_1200.png) |
|                                    |                 Trained for 1300 Iterations                  |                 Trained for 1200 Iterations                  |
|        A minion in a forest        | ![](images/Q2/image/a_minion_in_a_forest/output_a_iter_1500.png) | ![](images/Q2/image/a_minion_in_a_forest_guided/output_a_iter_1999.png) |
|                                    |                 Trained for 1500 Iterations                  |                 Trained for 2000 Iterations                  |





## 2.2 Texture Map Optimization for Mesh

|                   Initial Mesh                   |              Prompt: A porcupine               |              Prompt: A lion               |
| :----------------------------------------------: | :--------------------------------------------: | :---------------------------------------: |
| ![](images/Q2/mesh/a_porcupine/initial_mesh.gif) | ![](images/Q2/mesh/a_porcupine/final_mesh.gif) | ![](images/Q2/mesh/a_lion/final_mesh.gif) |



## 2.3 NeRF Optimization

|        Prompt        |                             RGB                              |                            Depth                             |
| :------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| A standing corgi dog | <img src="images/Q2/nerf/a_standing_corgi_dog/videos/rgb_ep_20.gif" alt="rgb_ep_20" style="zoom:400%;" /> | <img src="images/Q2/nerf/a_standing_corgi_dog/videos/depth_ep_20.gif" alt="rgb_ep_20" style="zoom:400%;" /> |





|        Prompt        |                             RGB                              |                            Depth                             |
| :------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| A standing corgi dog | <img src="images/Q2/nerf/a_standing_corgi_dog_guidance/videos/rgb_ep_10.gif" alt="rgb_ep_20" style="zoom:400%;" /> | <img src="images/Q2/nerf/a_standing_corgi_dog/videos/depth_ep_20.gif" alt="rgb_ep_20" style="zoom:400%;" /> |





