# CognitiveInference
CognitiveInference，认知推理、常识知识库、常识推理与常识推理评估的系统项目，以现有国内外已有的常识知识库为研究对象，从常识知识库资源建设和常识推理测试评估两个方面出发进行整理，并结合自己近几年来在逻辑性推理知识库的构建、应用以及理论思考进行介绍。具体包括已有常识知识库项目资源介绍、逻辑推理类知识库的项目实践集合、常识推理测试评估项目集合。

# 项目介绍
常识推理是人工智能的高级阶段，基于已有知识，运用知识推理机技术，完成限定领域决策行为，能够在充分减少人为劳动的同时，产生经济效益。例如，基于已知知识进行知识推理，采用如事件驱动传导路径等进行知识发现，能够辅助于业务的推理和辅助决策，在智能投研进行未知风险预警、在舆情分析中对公司进行舆论控制和监控。  
"逻辑知识库"+"逻辑推理机"的混合协作模式，是目前实现以上目的的重要方式。
"逻辑知识库"作为描述现实社会事件之间传导关联的库，需要在规模、质量，领域针对性三个方面入手进行解决。具体地，作者通过对自己所涉及的推理项目进行系统回顾，认为，推理类常识知识库，应该从垂直和横向两个维度出发进行构建。

# 一、纵向常识逻辑
上需要考虑的是类人的抽象和概括能力，这个需要抽象、概念性、上下位知识的构建。例如，作者对纵向常识逻辑，形成了以下工作:  
1、上下位关系图谱项目：HyponymyExtraction(https://github.com/liuhuanyong/HyponymyExtraction).  
上下位这种语义关系是整个词汇语义关系中的一个重要内容，通过上下位关系，可以将世间万物进行组织和练联系起来，对于增进人们对某一实体或概念的认知上具有重要帮助，自然语言文本中存储着大量的上下位关系知识，如经过语言专家编辑整理形成的概念语义词典，如同义词词林，中文主题概念词典，hownet等，也存在开放百科知识平台当中，有效地利用这些信息，能够支持多项应用基于知识概念体系，百科知识库，以及在线搜索结构化方式的词语上下位抽取。适用的场景为用户输入一个需要了解的词语，后台通过查询既定知识库，从百百科知识库，在线非结构化文本中进行抽取，形成关于该词语的上下位词语网络，并以图谱这一清晰明了的方式展示出来。

2、电商商品概念与销售知识图谱项目：GoodsKG(https://github.com/liuhuanyong/GoodsKG). 
 
项目以京东电商为实验数据来源，采集京东商品目录树，并获取其对应的底层商品概念信息，组织形成商品知识图谱。目前，该图谱包括有概念的上下位is a关系以及商品品牌与商品之间的销售sale关系共两类关系，涉及商品概念数目1300+，商品品牌数目约10万+，属性数目几千种，关系数目65万规模。该项目可以进一步增强商品领域概念体系的应用，对自然语言处理处理的几个下游应用带来帮助，如商品品牌识别，商品对象及属性级别情感分析，商品评价短语库构建，商品品牌竞争关系梳理等提供基础性的概念服务。

3、抽象知识图谱项目：AbstractKnowledgeGraph(https://github.com/liuhuanyong/AbstractKnowledgeGraph)
抽象知识图谱，目前规模50万，支持名词性实体、状态性描述、事件性动作进行抽象。目标于抽象知识，包括抽象实体，抽象动作，抽象事件。基于该知识图谱，可以进行不同层级的实体抽象和动作抽象，这与人类真实高度概括的认知是一致的。本项目提出了一个抽象知识图谱的项目，目的是对知识抽象与泛化提供一个思路并初步实践，介绍了抽象知识图谱，对抽象图谱的现实需求进行论述。介绍了中文抽象图谱的相关工作。摆阔CN-Probase,Hownet,大词林,百度百科Schema等，并给出了之前关联的项目地址。本项目提出了一个可用的抽象知识图谱构建路线，提出抽象知识图谱的实施路线并给出抽象接口实践。


# 二、横向常识逻辑 
横向上，需要挖掘顺承、因果、反转等多个方向的逻辑演化关系。例如，作者对横向常识逻辑，形成了以下下工作：  

4、因果事件图谱项目：CausalityEventExtraction(https://github.com/liuhuanyong/CausalityEventExtraction). 

以构造和总结因果模板，结合中文语言特点，构建因果语言知识库的方式，对因果事件抽取以及因果知识图谱构建进行尝试。本项目罗列出了9类显式因果逻辑抽取模式，通过使用因果连词库，结果词库、因果模式库等，完成因果抽取，对文本进行噪声移除，非关键信息去除等进行文本预处理，基于因果模式库，完成因果对抽取，选择选择一种恰当（短语、短句、句子主干）等方式进行事件表示。使用知识图谱中的实体对齐技术进行事件融合，基于业务需求，可以用相应的数据库进行存储，比如图数据库等完成事件存储。

5、顺承事件图谱项目：SequentialEventExtration(https://github.com/liuhuanyong/SequentialEventExtration). 

目前,以谓词性短语作为事件表示的方法方兴未艾,针对特定领域,构建起特定领域的顺承事件图谱,可以支持事件推理,基于事件的意图识别与推荐等多项运用。本项目基于50W文章领域语料,运用简单提取方式形成的顺承关系图谱demo,形成了事件节点为326781个, 顺承事件对为543580条,分别为30W和50W的图谱规模。

6、复合事件图谱项目：ComplexEventExtraction(https://github.com/liuhuanyong/ComplexEventExtraction). 
 
项目对中文复合事件抽取，包括条件事件、因果事件、顺承事件、反转事件等事件事件图谱的类型、表现形式进行了归纳，并结合复合事件模式与语料进行了实验。实验表明，反转事件，其实在某种程度上可以用来构造反义词词典，例如"不是A而是B"这种模式，可以得到很多反义的词或短语，我们可以用wordvector找相近词，可以靠这种方式收集反义词。汉语显示标记其实在中文文本当中还是用的很普遍，在1000W文本中，有超过半数的文本中包含以上模式。能够把显示事件图谱做好，感觉用处还是很多的。

# 三、常识逻辑推理

"逻辑推理机"是支配逻辑知识库的重要运算机器，通过对现有逻辑知识库，通过推理规则传导、知识关联路径匹配，完成对现有逻辑知识库的游走，最终实现单跳或多跳等后续事件的推理和预测，在这个方面，需要使用owl本体推理机、图数据库匹配、图数据库路径查找、推理规则配置、图结构预测等多种不同形式。与此同时，与逻辑推理关联的推理能力评估，也是检验常识推理智能的必要手段。例如，作者对常识逻辑推理，形成了一下工作：

7、基于问答社区的逻辑知识问答项目：ZhidaoChatbot(https://github.com/liuhuanyong/ZhidaoChatbot). 

本项目完成了一个基于线上问答社区的常识逻辑性问答机器人接口demo，本项目的问答机器人接口可以满足原因逻辑，结果逻辑，可以回答为什么，有了会怎么样等问题，也可以推荐相似性的问题，可以作为基于逻辑事理知识的一种补充，问答机器人接口可以作为开源实体性问答机器人的逻辑性问答补充，也可以为逻辑性知识库的构建提供帮助。

8、基于事理图谱的未来事件预测项目：EventPredictBasedOnEG(https://github.com/liuhuanyong/EventPredictBasedOnEG). 
 
基于海量数据进行因果挖掘,可以得到大量的因果知识，基于因果逻辑库,即历史因果,通过计算当前事件与历史事件的相似性，可以在定性的方式上做出一些方向性的预测，方向上包括两种，一种是积极信号，另一种是消极信号，本项目主要是想完成这一目标．介绍了一个基于因果图谱的既定事件未来预测的接口预测demo。

9、学迹事理实时知识库终身学习项目：EventKGNELL(https://github.com/liuhuanyong/EventKGNELL). 

事理图谱版Magi，EventKGNELL, event knowlege graph never end learning system, a event-centric knowledge base search system，一个7*24小时不断学习的实时事理学习与搜索平台，力图紧跟实时网络信息，面向公众提供以“事件”为核心的实时结构化知识搜索服务的实时事理逻辑知识库终身学习和事件为核心的知识库搜索项目，项目实现了包括事件概念抽取、事件因果逻辑抽取、事件数据关联推荐与推理，

本项目对现有国内外已有的常识知识库为研究对象，从常识知识库资源建设和常识推理测试评估两个方面出发进行整理，并结合自己近几年来在逻辑性推理知识库的构建、应用以及理论思考进行介绍。

# 开放常识知识库与常识推理评测项目

# 一、已有常识知识库资源集合 

| 大类 | 小类 | 名称 | 地址 |
| ----- | -------- | ------- | ------- |
| 语言学知识库  | 语言标注语料库  | Penn Treebank  | [点击查看](https://www.ldc.upenn.edu/) |
| 语言学知识库  | 语言标注语料库  | The Penn Discourse Tree- bank (PDTB)  | [点击查看](https://www.ldc.upenn.edu/) |
| 语言学知识库  | 语言标注语料库  | The Abstract Meaning Representation (AMR) corpus  | [点击查看](https://www.ldc.upenn.edu/) |
| 语言学知识库  | 词汇知识库  | WordNet  | [点击查看](https://wordnet.princeton.edu/) |
| 语言学知识库  | 词汇知识库  | VerbNet | [点击查看](https://verbs.colorado.edu/~mpalmer/projects/verbnet.html) |
| 语言学知识库  | 词汇知识库  | VerbOcean  | [点击查看](http://demo.patrickpantel.com/demos/verbocean/) |
| 语言学知识库  | 词汇知识库  | VerbCorner  | [点击查看](https://archive.gameswithwords.org/VerbCorner/about.php) |
| 语言学知识库  | 框架语义知识库  | FrameNet  | [点击查看](https://framenet.icsi.berkeley.edu/fndrupal/framenet_data) |
| 语言学知识库  | 框架语义知识库  | PropBank  | [点击查看](https://propbank.github.io/) |
| 语言学知识库  | 预训练语义向量  | GloVe  | [点击查看](https://nlp.stanford.edu/projects/glove/) |
| 语言学知识库  | 预训练语义向量  | FastText  | [点击查看](https://github.com/facebookresearch/fastText) |
| 语言学知识库  | 预训练语义向量  | wordpiece embeddings  | [点击查看](https://github.com/google-research/bert) |
| 常识库  | 常识库  | YAGO  | [点击查看](https://www.mpi-inf.mpg.de/departments/databases-and-information-systems/research/yago-naga/yago/downloads/) |
| 常识库  | 常识库  | DBpedia  | [点击查看](https://wiki.dbpedia.org/develop/datasets) |
| 常识库  | 常识库  | WikiTaxonomy  | [点击查看](https://www.h-its.org/en/research/nlp/wikitaxonomy/)|
| 常识库  | 常识库  | Freebase  | [点击查看](https://developers.google.com/freebase/) |
| 常识库  | 常识库  | NELL  | [点击查看](https://rtw.ml.cmu.edu/rtw/) |
| 常识库  | 常识库  | Probase  | [点击查看](https://concept.research.microsoft.com/Home/Download) |
| 常识库  | 常识库  | Wikidata  | [点击查看](https://www.wikidata.org/) |
| 常识知识库  | 常识知识库  | Cyc  | [点击查看](https://www.cyc.com/researchcyc/) |
| 常识知识库  | 常识知识库  | ConceptNet  | [点击查看](https://conceptnet.io/) |
| 常识知识库  | 常识知识库  | SenticNet  | [点击查看](https://sentic.net/downloads/) |
| 常识知识库  | 常识知识库  | Isanette and IsaCore  | [点击查看](https://sentic.net/downloads/) |
| 常识知识库  | 常识知识库  | COGBASE  | [点击查看](https://cogview.com/cogbase/) |
| 常识知识库  | 常识知识库  | WebChild.  | [点击查看](https://www.mpi-inf.mpg.de/departments/databases-and-information-systems/research/yago-naga/webchild/) |
| 常识知识库  | 常识知识库  | LocatedNear  | [点击查看](https://github.com/adapt-sjtu/commonsense-locatednear) |
| 常识知识库  | 常识知识库  | ATOMIC  | [点击查看](https://homes.cs.washington.edu/~msap/atomic/) |
| 常识知识库  | 常识知识库  | ASER  | [点击查看](https://hkustknowcomp.github.io/ASER/) |
| 常识知识库  | 常识知识库  | 学迹实时事理系统  | [点击查看](https://xueji.datahorizon.cn/) |

# 二、常识推理评测项目资源

| 大类 | 名称 | 作者 | 规模 | 网址 |
| ----- | ------- | ------- | -------- | ------- |
|Reference Resolution  | Winograd Schema Challenge | Morgenstern et al., 2016 | 60 |[点击查看](https://commonsensereasoning.org/winograd.html) |
|Reference Resolution  | WinoGrande | Sakaguchi et al., 2019 | 44.0K |[点击查看](https://mosaic.allenai.org/projects/winogrande) |
|Question Answering | MCTest.  | Richardson et al., 2013 | 2.00K |[点击查看](https://github.com/mcobzarenco/mctest/tree/master/) |
|Question Answering | RACE.  | Lai et al., 2017 | 97.7K |[点击查看](https://www.cs.cmu.edu/~glai1/data/race) |
|Question Answering | NarrativeQA. | Kocˇiský et al., 2018 | 46.8K |[点击查看](https://github.com/deepmind/narrativeqa) |
|Question Answering | ARC  | Clark et al., 2018 | 7.79K |[点击查看](https://data.allenai.org/arc/) |
|Question Answering | MCScript | Ostermann et al., 2018  | 13.9K |[点击查看](https://www.sfb1102.uni-saarland.de/?page_id=2582.) |
|Question Answering | ProPara | Mishra et al., 2018  | 488 |[点击查看](https://data.allenai.org/propara/.) |
|Question Answering | MultiRC. | Khashabi et al., 2018  | 9.87K  |[点击查看](https://cogcomp.org/multirc/) |
|Question Answering | ARCT | Habernal et al., 2018  | 2.45K  |[点击查看](https://github.com/UKPLab/argument-reasoning-comprehension-task.) |
|Question Answering | SQuAD. | Rajpurkar et al., 2018  | 151K  |[点击查看](https://rajpurkar.github.io/SQuAD-explorer/) |
|Question Answering | CoQA. | Reddy et al., 2018 | 8.40K  |[点击查看](https://stanfordnlp.github.io/coqa/) |
|Question Answering | QuAC.  | Choi et al., 2018 | 98.4K  |[点击查看](https://quac.ai/) |
|Question Answering | OpenBookQA.  | Mihaylov et al., 2018  | 5.96K  |[点击查看](https://github.com/allenai/OpenBookQA) |
|Question Answering | CommonsenseQA  | Talmor et al., 2019  | 9.40K  |[点击查看](https://www.taunlp.org/commonsenseqa.) |
|Question Answering | DREAM.  | Sun et al., 2019 | 10.2K  |[点击查看](https://dataset.org/dream/) |
|Question Answering | DROP.  | Dua et al., 2019  | 96.6K  |[点击查看](https://allennlp.org/drop.) |
|Question Answering | Cosmos QA.  | Huang et al., 2019 | 35.6K |[点击查看](https://wilburone.github.io/cosmos/) |
|Question Answering | MC-TACO.  | Zhou et al., 2019 | 1.89K |[点击查看](https://leaderboard.allenai.org/mctaco/submissions/public.) |
|Textual Enatailment  | RTE Challenges.  | Bentivogli et al., 2011  | 48.8K |[点击查看](https://tac.nist.gov/) |
|Textual Enatailment  | Conversational Entailment.  | Zhang & Chai, 2009 | 875 |[点击查看](https://github.com/lairmsu/ConversationalEntailment) |
|Textual Enatailment  | SICK.  | Marelli et al., 2014a | 9.84K |[点击查看](https://clic.cimec.unitn.it/composes/sick.html.) |
|Textual Enatailment  | SNLI.  | Bowman et al., 2015 | 570K |[点击查看](https://nlp.stanford.edu/projects/snli/) |
|Textual Enatailment  | SciTail.  | Khot et al., 2018 | 27.0K |[点击查看](https://data.allenai.org/scitail/) |
|Textual Enatailment  | SherLIiC.  | Schmitt & Schütze, 2019 | 3.99K |[点击查看](https://github.com/mnschmit/SherLIiC.) |
|Plausible Inference  | COPA.  | Roemmele et al., 2011 | 1.00K |[点击查看](https://people.ict.usc.edu/~gordon/copa.html.) |
|Plausible Inference  | CBT.  | Hill et al., 2015  | 687K  |[点击查看](https://research.fb.com/downloads/babi/) |
|Plausible Inference  | ROCStories.  | Mostafazadeh et al., 2016 | 98.2K |[点击查看](https://cs.rochester.edu/nlp/rocstories/) |
|Plausible Inference  | LAMBADA.  | Paperno et al., 2016 | 10.0K |[点击查看](https://zenodo.org/record/2630551#.XS5JHuhKhPZ.) |
|Plausible Inference  | JOCI.  | hang et al., 2017 | 39.1K |[点击查看](https://github.com/sheng-z/JOCI) |
|Plausible Inference  | CLOTH.  | Xie et al., 2017 | 99.4K |[点击查看](https://www.cs.cmu.edu/~glai1/data/cloth/.) |
|Plausible Inference  | SWAG.  | Zellers et al., 2018 | 114K |[点击查看](https://rowanzellers.com/swag/.) |
|Plausible Inference  | ReCoRD.  | Zhang et al., 2018 | 121K |[点击查看](https://sheng-z.github.io/ReCoRD-explorer/) |
|Plausible Inference  | HellaSWAG.  | Zellers et al., 2019a | 70.0K |[点击查看](https://rowanzellers.com/hellaswag/.) |
|Plausible Inference  | AlphaNLI.  | Bhagavatula et al., 2019 | 171K |[点击查看](https://leaderboard.allenai.org/anli/submissions/get-starte) |
|Intuitive Psychology  | Triangle-COPA.  | Gordon, 2016  | 100 |[点击查看](https://github.com/asgordon/TriangleCOPA.) |
|Intuitive Psychology  | Story Commonsense.  | Rashkin et al., 2018a  | 161k |[点击查看](https://uwnlp.github.io/storycommonsense/.) |
|Intuitive Psychology  | Event2Mind.  | Rashkin et al., 2018b  | 57.1K |[点击查看](https://uwnlp.github.io/event2mind/.) |
|Intuitive Psychology  | SocialIQA.  | Sap et al., 2019b | 44.8K |[点击查看](https://maartensap.github.io/social-iqa/.) |
|Multple Tasks  | bAbI.  | Weston et al., 2016 | 40.0K |[点击查看](https://research.fb.com/downloads/babi/.) |
|Multple Tasks  | Inference is Everything.  | - | - |[点击查看](https://github.com/decompositional-semantics-initiative/DNC.) |
|Multple Tasks  | GLUE.  | - | - |[点击查看](https://glueBechmark.com/tasks.) |
|Multple Tasks  | DNC.  | Poliak et al., 2018a | 570K |[点击查看](https://github.com/decompositional-semantics-initiative/DNC.) |
|Multple Tasks  | SuperGLUE.  | - | - |[点击查看](https://super.glueBechmark.com/.) |

# 关于作者

刘焕勇， Liu Huanyong，2017年硕士毕业，目前就职于中国科学院软件研究所，专注金融、情报两大领域，从事事件抽取、事件演化、情感分析、事理（知识）图谱、常识推理、语言资源构建与应用等研发工作。主持研发自然语言处理技术开放平台数地工场、大规模实时事理知识学习系统学迹、全行业因果链查询与溯源项目寻链系统，并在智能金融、智能情报落地中负责实施了多个项目。致力于面向中文处理的基础知识库建设与理论技术开源共享，目前累计对外开放自然语言处理实践项目六十余个，在openkg开放知识图谱联盟中开放工业应用知识库七类，主笔数地工场技术类系列文章二十余篇。

如有自然语言处理、知识图谱、事理图谱、社会计算、语言资源建设等问题或合作，可联系我：        
1、我的自然语言处理开源项目：https://liuhuanyong.github.io     
2、我的csdn技术博客：https://blog.csdn.net/lhy2014    
3、我的联系方式: 刘焕勇，中国科学院软件研究所，lhy_in_blcu@126.com.    
4、我的共享知识库项目：刘焕勇，事理类知识库数据集，http://www.openkg.cn/organization/datahorizon.   
5、我的工业项目：刘焕勇，以事理为核心的金融情报探索：https://datahorizon.cn.         
