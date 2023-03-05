#!/bin/bash

# 提示用户输入要操作的容器名
read -p "请输入要操作的容器名: " container_name

# 停止运行中的容器
docker stop $container_name

# 删除原有的容器
docker rm $container_name

# 提示用户输入要更新的镜像名称和版本号
read -p "请输入要更新的镜像名称: " image_name
read -p "请输入要更新的镜像版本号: " image_version

# 获取最新的镜像
docker pull $image_name:$image_version

# 启动新的容器
docker run -d --name $container_name $image_name:$image_version

echo "容器更新完成！"
