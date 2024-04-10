






```

docker run -it -u root --name=mindie_server_t35 --net=host --ipc=host \
--device=/dev/davinci0 \
--device=/dev/davinci1 \
--device=/dev/davinci2 \
--device=/dev/davinci3 \
--device=/dev/davinci4 \
--device=/dev/davinci5 \
--device=/dev/davinci6 \
--device=/dev/davinci7 \
--device=/dev/davinci_manager \
--device=/dev/devmm_svm \
--device=/dev/hisi_hdc \
-v /usr/local/Ascend/driver:/usr/local/Ascend/driver \
-v /usr/local/Ascend/add-ons/:/usr/local/Ascend/add-ons/ \
-v /usr/local/sbin/:/usr/local/sbin/ \
-v /var/log/npu/slog/:/var/log/npu/slog \
-v /var/log/npu/profiling/:/var/log/npu/profiling \
-v /var/log/npu/dump/:/var/log/npu/dump \
-v /var/log/npu/:/usr/slog \
-v /etc/hccn.conf:/etc/hccn.conf \
-v /home:/workspace \
mindie_server:1.0.T35 \
/bin/bash


docker exec -it mindie_server_t35 bash


/home/HwHiAiUser/mindie-service_1.0.RC1_linux-aarch64/bin

cp -r /workspace/token_input_gsm.csv .



vim conf/config.json 


cd /workspace/aicc/model_from_hf/chatglm3-6b-chat


/workspace/aicc/model_from_hf/Baichuan2-7B-Chat


---

/home/HwHiAiUser/atb-models/examples/convert


convert_weights.py


使用${llm_path}/examples/convert/convert_weights.py将bin转成safetensor格式


示例
python ${llm_path}/examples/convert/convert_weights.py --model_path ${weight_path}
输出结果会保存在bin权重同目录下


/home/HwHiAiUser

source  set_env.sh 


python examples/convert/convert_weights.py --model_path /workspace/aicc/model_from_hf/Baichuan2-7B-Chat --from_pretrained False

python examples/convert/convert_weights.py --model_path /workspace/aicc/model_from_hf/Baichuan2-7B-Chat 





---




启动脚本

Flash Attention的启动脚本路径为${llm_path}/examples/run_fa.py

Page Attention的启动脚本路径为${llm_path}/examples/run_pa.py
```


