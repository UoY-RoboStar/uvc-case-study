This repository contains a RoboChart model for risk analysis of an agriculture robot providing UV light-treatment and a latest verification result in the folder [prism-gen](prism-gen). 

The model is probabilistic, and created in [RoboTool](https://robostar.cs.york.ac.uk/robotool/). The properties to be verified are inside the folder [Properties](Properties).

The model is also analysed in RoboTool by automatically 
1. translating it to a [PRISM](https://www.prismmodelchecker.org/) [model](prism-gen/system.prism),
2. translating the [properties](Properties/uvc.assertions) to the [PRISM properties](prism-gen/20230314214811/uvc_assertions.props),  
3. launching many PRISM model checker instances to verify properties, and 
4. collecting results (from log files such as [this one](prism-gen/20230314214811/P_dangerous_C20_noOds_aware_t-4_modUVC_ctrlUVC_stm_213.log)) and generating a [report](prism-gen/20230314214811/uvc_assertions.html).

Please refer to this paper "[Probabilistic modelling and verification using RoboChart and PRISM](http://dx.doi.org/10.1007/s10270-021-00916-8)" for more information about the probabilistic modelling and verification for RoboChart.

The information about how to install RoboTool, open this model, and verify it in RoboTool can be found in the [RoboTool manual](https://robostar.cs.york.ac.uk/publications/techreports/reports/robotool-manual.pdf). In particular, the plugins in the categories PRISM, RoboChart, RoboChart Generator, and Epsilon should be installed, and the chapter "Model Checking with PRISM" should be referred to.
