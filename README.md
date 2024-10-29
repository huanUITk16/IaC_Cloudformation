# IaC_Cloudformation
Cloudformation in implement AWS infrastructure

[CÁCH TRIỂN KHAI HẠ TẦNG AWS DỰA VÀO MÃ NGUỒN NÀY]

1. Clone source code về local bằng git command 
   git clone https://github.com/huanUITk16/IaC_Cloudformation.git
2. Tạo S3 Bucket trên AWS Console
3. Upload các file module .yml lên trên S3 Bucket. Ví dụ upload module VPC lên S3, upload file modules/vpcmodule.yml. Tương tự cho các module EC2 và SecurityGroup
4. Sau khi upload 3 modules cần thiết lên S3, cập nhật templateURL của các module vào file template Nestedstack.yml -> upload Nestedstack.yml lên S3
5. Tạo Stack bằng service CloudFormation của AWS bằng URL của Nestedstack.yml vừa upload lên s3
