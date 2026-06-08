# UATR-benchmark
code for "Deep Learning for Underwater Acoustic Target Recognition: A Comprehensive Review, Benchmarking and Future Directions"

## 如何用 Codex 快速看懂这个仓库

### 1) 推荐模式（先读后跑）
- **阶段一：只读/问答模式（不改代码）**
  - 目标：先搞清目录、入口、模块关系。
  - 明确要求：`只读，不修改任何文件`。
- **阶段二：Agent 模式（可执行命令）**
  - 目标：让 Codex 帮你追调用链、解释训练/测试流程、检查某个方法的输入输出。
  - 同样建议先加约束：`不要改代码，只分析并解释`。

### 2) 高质量提示词模板（每次都带这三点）
- **目标**：你要看懂什么（架构/模块/调用链）
- **范围**：限定目录或文件
- **输出格式**：比如“先总览，再分点，再给阅读顺序”

### 3) 可直接复制的提示词（已按本仓库目录定制）
- 先定义两个占位符，后面的模板直接复用：  
  - `<repo_root_absolute_path>`：仓库绝对路径（示例：`/home/user/projects/UATR-benchmark` 或 `C:\Users\user\UATR-benchmark`）  
  - `<methods_dir_path>`：相对仓库根目录的子目录名，取值为 `Deep Learning for Underwater Acoustic Target Recognition A Comprehensive Review, Benchmarking and Future Directions`（这是仓库当前真实目录名）  
  - 路径中有空格时，建议在命令或提示词中整体加反引号或引号。

#### A. 仓库总览
请只读，不修改任何文件。基于 `<repo_root_absolute_path>` 给我一个新手友好的仓库总览：  
1. 顶层目录作用  
2. `<methods_dir_path>` 下各子目录（如 `AMNet`、`CMOE`、`DINOV2`、`MFCC+RACNN`、`UATC-Densenet`）各自做什么  
3. 每个方法目录里 `train.py`、`test.py`、`model.py`、`dataset.py` 的职责  
最后给我一个从易到难的阅读顺序。

#### B. 单模块精读（示例：AMNet）
请只分析  
`<repo_root_absolute_path>/<methods_dir_path>/AMNet`，不要修改代码。  
按文件说明职责、主要类/函数、输入输出、依赖关系；最后给我这个模块最小执行路径（从数据到模型到训练/测试）的文字版流程。

#### C. 调用链追踪（示例：训练流程）
请从  
`<repo_root_absolute_path>/<methods_dir_path>/AMNet/train.py`  
开始，追踪训练阶段的关键调用链（函数名 + 所在文件），按执行顺序解释每一步做了什么、依赖哪些配置或数据。

#### D. 边读边学（文件逐段解释）
请逐段讲解  
`<repo_root_absolute_path>/<methods_dir_path>/DINOV2/model.py`，不要改代码。  
每段都回答：这段在解决什么问题？输入输出是什么？和前后段怎么衔接？有哪些容易踩坑的点？

### 4) 建议学习节奏
1. 先做一次“仓库总览”  
2. 选一个目录做“单模块精读”  
3. 对 `train.py` 做“调用链追踪”  
4. 对 `model.py` 做“逐段讲解”  
5. 最后让 Codex “根据我的复述纠错并补漏”
