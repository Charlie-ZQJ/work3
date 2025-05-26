# 钟泉江 324080203115 24机械1班 谢海彬 324085503321 24机械3班 github：(https://github.com/Charlie-ZQJ/work2)
# 二手车价格预测系统
## 项目描述
基于线性回归算法的二手车价格预测系统，通过分析车辆行驶里程与价格的关系构建预测模型。包含完整的数据清洗、可视化分析和模型评估流程。
## 目录结构

car-price/
├── data/
│    └── used_cars.csv 
├── car-price.ipynb 
└── README.md

## 依赖包与环境配置
库名称	功能	建议版本
pandas	数据读取与清洗	≥1.3.0
numpy	数值计算与数组操作	≥1.21.0
scikit-learn	线性回归模型训练	≥1.0.0
matplotlib	数据可视化（散点图）	≥3.4.0
seaborn	数据可视化（热力图）	≥0.11.0
## 运行说明
确保本地有used_cars.csv数据集
修改代码中pd.read_csv的路径为本地实际路径，例如：df = pd.read_csv('D:/Users/Desktop/car-price/data/used_cars.csv')。
点击全部运行，程序将自动完成以下流程：
数据读取→清洗→相关性分析→模型训练→效果评估→预测输出。
## 结果说明与截图示例
运行代码后，将生成以下关键输出：
1、相关性热力图

![image](https://github.com/user-attachments/assets/81f75f71-886a-4669-9fe2-e97d54e0fbb3)

展示model_year（车龄）、milage（里程）、price（价格）的皮尔逊相关系数。
2、模型拟合效果散点图

![image](https://github.com/user-attachments/assets/884b661d-3004-493d-8479-b2dbade515fc)

蓝色散点为原始数据（里程 - 价格关系），红色直线为线性回归模型的拟合结果。
3、结果截图

![image](https://github.com/user-attachments/assets/b69678bb-5aa3-4d60-96c6-1e7dfa69acfa)

终端最后输出对75,000英里车辆的预测价格，可通过修改mileage_new参数预测其他里程的车辆价格：
## 改进方向
特征扩展：加入brand（品牌）、condition（车况）等特征，提升模型解释力。
模型优化：使用PolynomialFeatures进行多项式回归，捕捉非线性关系。

