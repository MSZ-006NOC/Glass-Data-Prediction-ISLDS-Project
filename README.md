# ISLDS-Project---Glass-Data-Prediction
## ReadME
- This project is based on the "Introduction to Statistical Learning and Data Science" (ISLDS) course taught by Professor Li Xia at the South China University of Technology, School of Mathematics in Spring 2023. The project is a course design assignment.
- The goal of the project is to predict specific glass properties (e.g., density, Abbe number, refractive index, transition temperature, or Young's modulus) based on an open-source dataset of glass properties. The main approach involves building predictive models using statistical learning techniques, leveraging oxide composition data from the dataset.
- The original course guidelines suggested excluding halide and  chalcogenide glass properties and recommended focusing on oxide composition rather than single-element composition for modeling and prediction.
- In this project, I processed the oxide composition data and utilized Random Forest (RF) and Support Vector Machine (SVM) methods to predict glass density.
- For details on data preprocessing, analysis, modeling, result analysis, and interface demonstration, please refer to the `Project-Presentation.html` file.
- The dataset can be found in the `Dataset` folder.
- Relevant images are available in the `Image` folder.
- Models for Random Forest and Support Vector Machine are stored in the `Model` folder.
- Opensource dataset
    - [SciGlass](https://github.com/epam/SciGlass)
    - [GlassPy](https://github.com/drcassar/glasspy)

## README_CN
- 此项目相关课程为统计学习与数据科学导论（华南理工大学数学学院）2023年春季，夏立教授主讲。项目为课程设计
- 项目目标是针对开源玻璃性质数据集，从中挑选一些玻璃性质（如密度，阿贝数，折射率，转变温度或杨氏模量）进行预测。基本方法是基于数据集中氧化物的成分，利用统计学习模型进行建模然后预测玻璃性质
- 原课程设计指导中提到可以排除卤化物和制冷剂玻璃性质，同时尽量使用氧化物成分而不是单一元素成分进行建模然后预测
- 个人是使用了氧化物成分处理然后建模，使用随机森林(RF, Random forest)与支持向量机(SVM, Support Vector Machine)方法对密度进行预测
- 数据预处理，数据分析，建模分析，结果分析，演示接口详见`Project-Presentation.html`文件
- 数据集详见`Dataset`文件夹
- 相关图片见`Image`文件夹
- 随机森林与支持向量机模型见`Model`文件夹
- 开源数据集链接
    - [SciGlass](https://github.com/epam/SciGlass)
    - [GlassPy](https://github.com/drcassar/glasspy)
- 如果这个仓库能帮助到后续的同学作为参考，那真的太好了，毕竟做课设大家都挺头疼的是吧哈哈哈（求一个star）

## Results Display
### Feature and response variable histograms and scatter plots
<p align="center">
  <strong style="font-size: 20px;">Histogram Plot</strong><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/hist.png" alt="Histogram Plot" style="width: 600px; height: auto; margin-top: 10px;">
</p>


## Oxygen compound scatter plot
<p align="center">
  <strong style="font-size: 20px;">SiO2</strong><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/sio2.png" alt="Histogram Plot" style="width: 500px; height: auto; margin-top: 10px;">
</p>
<p align="center">
  <strong style="font-size: 20px;">GeO2</strong><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/geo2.png" alt="Histogram Plot" style="width: 500px; height: auto; margin-top: 10px;">
</p>
<p align="center">
  <strong style="font-size: 20px;">Ga2O3</strong><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/ga2o3.png" alt="Histogram Plot" style="width: 500px; height: auto; margin-top: 10px;">
</p>

## Experimental Results

<table style="margin: auto; text-align: center; width: 80%; font-size: 20px;">
<caption>Nonlinear SVM regression prediction<strong></caption>
<tr>
    <th style="text-align: center;">R2 score</th>
    <th style="text-align: center;">MSE score</th>
    <th style="text-align: center;">MAE score</th>
</tr>
<tr>
    <td style="text-align: center;">0.8557</td>
    <td style="text-align: center;">0.2133</td>
    <td style="text-align: center;">0.22259</td>
</tr>
</table>


<p>
  <strong style="font-size: 20px;"><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/svm_scatter.png" alt="Histogram Plot" style="width: 400px; height: auto; margin-top: 10px;">
</p>
<p>
  <strong style="font-size: 20px;"><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/svm_residual.png" alt="Histogram Plot" style="width: 400px; height: auto; margin-top: 10px;">
</p>



<table style="margin: auto; text-align: center; width: 80%; font-size: 20px;">
<caption>Random forest regression<strong></caption>
<tr>
    <th style="text-align: center;">R2 score</th>
    <th style="text-align: center;">MSE score</th>
    <th style="text-align: center;">MAE score</th>
</tr>
<tr>
    <td style="text-align: center;">0.8678</td>
    <td style="text-align: center;">0.196</td>
    <td style="text-align: center;">0.204</td>
</tr>
</table>

<p>
  <strong style="font-size: 20px;"><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/forest_scatter.png" alt="Histogram Plot" style="width: 400px; height: auto; margin-top: 10px;">
</p>
<p>
  <strong style="font-size: 20px;"><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/forest_residual.png" alt="Histogram Plot" style="width: 400px; height: auto; margin-top: 10px;">
</p>
