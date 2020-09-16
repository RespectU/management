# management
aws ecr get-login-password --region ap-northeast-2 | docker login --username AWS -p $(aws ecr get-login-password --region ap-northeast-2) 271153858532.dkr.ecr.ap-northeast-2.amazonaws.com/
