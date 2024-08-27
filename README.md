# DATA_Govern
## 数据架构 （数据分级）
L1到L3的过程中隐藏着一个问题，对质量分数的监控处于黑箱，用户是不直接参与的我
这导致对数据质量的监控存在无法覆盖的问题 数据准入的问题。比如用一个确定的工具去定义用户传入的数据能够解析出多少有效数据？定义有多少细胞数产出，每个细胞多少基因，比如能否有明显的免疫细胞分群。这里有一组工具


- L3是确定的工具对基础的生物数据的去除噪声的整合，结果是带有专家知识的测序数据的信息的数字化表示，带有注释的测序的矩阵。


- L4的定义是对于带有注释的矩阵的专家经验（人在回路的）介入的对原始矩阵信息实现的数据治理。输入是带有基因表达谱信息注释的矩阵，输出是专家经验的对矩阵去除噪声的一组细胞的每个细胞的基因表达谱的信息的数字化实体。

- L5定义的知识是业务的终极目标，叫做knowledeg或者研究结果，这里的数据实体如何定义，之前的数据实体是由其固定的。这里的数据实体是在L4：无/弱噪声的基础上，借助特定工具集，在专家经验的推导下，对L4的高纬度信息的低纬表示中的无序信息作出定义。


这样看，L1到L5都会承担数据分发服务的责任，L5数据的交付，形式是H5，


### L3 - 注释与整合的数字化表示
	-  定义: 通过确定的生物信息学工具，对基础生物数据（如原始测序数据）进行去噪和整合，结果是带有专家知识注释的测序数据的数字化表示。这些数据通常表现为带有注释的测序矩阵，例如基因表达谱矩阵。
	- 数据实体: 带有详细注释的基因表达矩阵，代表每个条形码/细胞在不同基因上的表达量。这些矩阵经过基础去噪处理，包含了生物学上有意义的特征。
### L4 - 数据治理与专家介入
	- 定义: 在带有注释的矩阵基础上，专家通过经验和知识对数据进行进一步治理。此过程可能包括去除残余噪声、数据标准化、特征选择或识别并排除不符合预期的样本。专家的介入使数据更加精炼和准确，从而形成一组无/弱噪声的细胞基因表达谱的数字化实体。
	- 数据实体: 高质量、专家校验后的基因表达矩阵。这些矩阵经过数据治理和进一步的去噪处理，代表了一组细胞的精确基因表达谱，是后续高级分析的基础。
### L5 - 知识生成与研究成果
	- 定义: 在L4层的高质量数据基础上，借助特定工具集和专家经验，通过对高维信息的低维表示进行分析，生成无序信息的有序表示，最终得出有价值的研究结论或业务目标。L5层的数据实体是在专家推导和高级算法的指导下，从复杂数据中提取的、与研究目标直接相关的知识或结论。
	- 数据实体: 高度凝练和解释的知识表示。这些实体可能包括研究论文中的结论、科学发现、预测模型、特定基因与表型的关联分析结果等。这一层的数据实体不再是简单的矩阵，而是高层次的研究成果或业务决策支持。

	- L3: 带有注释的数字化测序矩阵，代表基础生物数据的去噪和整合结果。
	- L4: 经过专家治理和优化的基因表达矩阵，具有更高的准确性和精度，为高级分析提供可靠的基础。
	- L5: 基于L4数据生成的研究结论或业务目标的知识表示，反映了研究或分析的最终成果。


![singlecell_dataflow drawio(3)](https://github.com/user-attachments/assets/bc193137-5d69-4670-9992-439fb7ef9088)
