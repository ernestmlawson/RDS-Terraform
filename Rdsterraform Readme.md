# RDS using Terraform 
provider "aws" {
  region     = "us-east-1"
}
resource "aws_db_instance" "default" {
  allocated_storage    = 10
  storage_type         = "gp2"
  engine               = "oracle-se"
  instance_class       = "db.t2.micro"
  name                 = "db"
  username             = "username"
  password             = "password"
}
