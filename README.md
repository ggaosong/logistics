课堂作业：rag物流知识库
部署：
1.在linux主机上克隆
git clone https://github.com/ggaosong/logistics.git

2.添加 huggingface 镜像环境变量
export HF_ENDPOINT=https://hf-mirror.com

3.下载大模型，不要下载量化版，效果差，回无反馈
cd logistics
git clone https://www.modelscope.cn/ZhipuAI/chatglm2-6b.git $PWD/chatglm2-6b

4.下载向量模型
huggingface-cli download --resume-download moka-ai/m3e-base --local-dir ./m3e-base

5.项目修改
需要根据下载目录进行修改，2个模型和向量数据库目录根据实际情况修改

6.项目运行
A.先运行get_vector.ipynb,运行完毕终止内核，释放CPU
B.然后运行model.ipynb，测试模型运行,运行完毕终止内核，释放GPU
C.最后运行main.ipynb，查看运行结果

7.总结
只要给足够的文档，智能知识库就可以私有化部署


