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
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/hist.png" alt="Histogram Plot" style="width: 1200px; height: auto; margin-top: 10px;">
</p>


## Oxygen compound scatter plot
<p align="center">
  <strong style="font-size: 20px;">SiO2</strong><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/sio2.png" alt="Histogram Plot" style="width: 1200px; height: auto; margin-top: 10px;">
</p>
<p align="center">
  <strong style="font-size: 20px;">GeO2</strong><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/geo2.png" alt="Histogram Plot" style="width: 1200px; height: auto; margin-top: 10px;">
</p>
<p align="center">
  <strong style="font-size: 20px;">Ga2O3</strong><br>
  <img src="https://raw.githubusercontent.com/MSZ-006NOC/Glass-Data-Prediction-ISLDS-Project/main/Image/ga2o3.png" alt="Histogram Plot" style="width: 1200px; height: auto; margin-top: 10px;">
</p>

## Experimental Results
<style>
  table {
    margin-left: auto;
    margin-right: auto;
    width: 30%; /* 设置表格宽度为80% */
    height: 80px; /* 设置表格高度为200像素 */
    text-align: center; /* 将表格中的文本内容居中对齐 */
  }
  th, td {
    font-size: 20px; /* 设置文字大小为16像素 */
    font-weight: bold; /* 设置文字加粗 */
  }
  caption {
    font-size: 24px; /* 设置标题文字大小为20像素 */
    font-weight: bold; /* 设置标题文字加粗 */
    margin-bottom: 10px;
  }
</style>
<table>
  <caption>Nonlinear SVM regression prediction</caption>
  <tr>
    <th>R2 score</th>
    <th>MSE score</th>
    <th>MAE score</th>
  </tr>
  <tr>
    <td>0.8557</td>
    <td>0.2133</td>
    <td>0.22259</td>
  </tr>
</table>
<style>
  .image-with-padding {
    padding-right: 30px; /* 设置图片右侧间隔为10像素 */
  }
  .component {
    margin-top: 20px; /* 设置组件上方距离为20像素 */
  }
</style>
<div align="center" class="component"><img src='image/svm_scatter.png'class="image-with-padding" alt="Image 1"><img src='image/svm_residual.png' alt="Image 2"></div>

<style>
  table {
    margin-left: auto;
    margin-right: auto;
    width: 30%; /* 设置表格宽度为80% */
    height: 80px; /* 设置表格高度为200像素 */
    text-align: center; /* 将表格中的文本内容居中对齐 */
  }
  th, td {
    font-size: 20px; /* 设置文字大小为16像素 */
    font-weight: bold; /* 设置文字加粗 */
  }
  caption {
    font-size: 24px; /* 设置标题文字大小为20像素 */
    font-weight: bold; /* 设置标题文字加粗 */
    margin-bottom: 10px;
  }
</style>
<table>
  <caption>Random forest regression</caption>
  <tr>
    <th>R2 score</th>
    <th>MSE score</th>
    <th>MAE score</th>
  </tr>
  <tr>
    <td>0.8678</td>
    <td>0.196</td>
    <td>0.204</td>
  </tr>
</table>
<style>
  .image-with-padding {
    padding-right: 30px; /* 设置图片右侧间隔为10像素 */
  }
  .component {
    margin-top: 20px; /* 设置组件上方距离为20像素 */
  }
</style>
<div align="center" class="component"><img src='image/forest_scatter.png'class="image-with-padding" alt="Image 1"><img src='image/forest_residual.png' alt="Image 2"></div>
